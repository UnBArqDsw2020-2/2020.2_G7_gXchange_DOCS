# Arquiteturas Alternativas

## Propósito

<p style="text-indent: 20px; text-align: justify">
O propósito deste documento é propor arquiteturas alternativas para o gXchange. Este documento não segue um rigor como o DAS, mas pode servir de consulta para possíveis migrações de arquitetura.
</p>

<p style="text-indent: 20px; text-align: justify">
Até o momento, a arquitetura do proposta do gXchange, que leva em conta os seus atributos de qualidade, é monolítica e com comunicação Cliente-Servidor. Algumas possíveis arquiteturas deste documento vão propor, de uma maneira geral, quais atributos de qualidade elas afetam.
</p>

## Microfrontend

### Problema

<p style="text-indent: 20px; text-align: justify">
Atualmente a arquitetura proposta para o gXchange conta com dois Front-ends, que de certo modo são muitos semelhantes e mantém componentes em comum, mas ainda sim, são muito coesos no que fazem. Muitos desses componentes podem ser exportados como um pacote de componentes, visto que a proposta é dos dois seguirem a mesma folha de estilo.
</p>

<p style="text-indent: 20px; text-align: justify">
Só que ao pensar na ideia de desenvolver o gXchange em um time grande e/ou poupar recursos do deploy e/ou adicionar um novo front-end com um objetivo diferente dos outros. Nesse último caso pode ser necessário replicar novamente os componentes, alocar mais recursos no Deploy.
</p>

### Abordagem

<p style="text-indent: 20px; text-align: justify">
A ideia é utilizar o padrão de micro frontends, que consiste na separação do front end em projetos menores, cada qual com seus propósitos. Ou seja, permite separar os times em projetos menores, que por sua vez possuem baixo acoplamento e alta coesão.
</p>

#### Vantagens

##### Vários projetos

<p style="text-indent: 20px; text-align: justify">
Com a separação em vários projetos menores, fica mais fácil para o time manter, e até para inserir novos membros no time. Muito menos código e e componentes bem desacoplados. Times não precisam se preocupar muito com os outros microfrontends apenas com o que eles estão mexendo.
</p>

##### Deploy Independente

<p style="text-indent: 20px; text-align: justify">
Cada um dos projetos pode ser deployado em um servidor diferente, e isso não afeta a comunicação e a montagem final dos componentes no sistema. E permite controles maiores até em níveis de escala e restrições de acesso.
</p>

### Exemplo

<p style="text-indent: 20px; text-align: justify">
Na imagem abaixo, segue uma representação bem simples de como é um microfrontend, para o usuário final há poucas diferenças, mas para o time de desenvolvimento cada um desses componentes é um front separado.
</p>

![MicroFrontend](../../assets/notas_arq/microfrontend.png)

## Microsserviços

<p style="text-indent: 20px; text-align: justify">
É notável que a arquitetura monolítica provida para o gXchange impacta negativamente na escalabilidade. Uma maneira de escalar e obter maior controle de quais componentes precisam de mais recursos em detrimento de outros. A arquitetura de microsserviços também beneficia a implementação de novas funcionalidades e pode servir para caso a aplicação comece a ficar complexa.
</p>

### Problemas

<p style="text-indent: 20px; text-align: justify">
Migrar para uma arquitetura de microsserviços tem vários pontos importantes, e neste caso não parece ser diferente. Segue uma lista de problemas:</p>

- Os componentes são muito acoplados
- As entidades User e Offer no banco são relacionadas a muitas outras e a separação por contextos não é facilitada
- De certo modo os dados precisam de uma interface, já que o Django utiliza até então um mapeamento ORM.

### Shared Database Pattern 

<p style="text-indent: 20px; text-align: justify">
O padrão de bancos de dados compartilhados consegue resolver parte do problema encontrado nessa divisão, a ideia consiste em separar os serviços e utilizar um banco de dados compartilhados com todos eles. Surge outros problemas, dentre eles: "Quem controla os dados?" e também "Será que realmente faz sentido centralizar tudo?" e por último "Quem pode escrever e ler?". Muitas Vezes um dado serviço só quer ler um dado, ou um conjunto de dados, ele não precisa editar aquele dado.   
</p>

![Shared Database](https://ebrary.net/htm/img/29/477/29.png)

<p style="width: fit-content; margin: 0 auto; font-size: 12px">"Shared Database Integration", Ebrary.net. Disponível em: <a href="https://ebrary.net/54032/economics/shared_database_integration" target="_blank" rel="noopener noreferrer">https://ebrary.net/54032/economics/shared_database_integration</a></p>

### Reporting Database Pattern

<p style="text-indent: 20px; text-align: justify">
A ideia aqui é que sempre que houver a necessidade de um serviço acessar os dados de outro serviço este padrão pode ser usado. Consiste em replicar o banco de um serviço e essa réplica é pública, para os outros serviços ou até externamente (não é elegante deixar bases abertas publicamente), e parte mais importante, ela só permite leituras. As alterações da base de dados principal são propagadas para a base pública sempre que houver uma mudança.  
</p>

<p style="text-indent: 20px; text-align: justify">
Para o contexto de diminuir a quantidade de requisições de leitura de um serviço, que gerariam uma demanda maior, esse padrão pode ser aproveitado pois muito dos outros serviços realizam apenas leituras.
</p>

#### Serviços que precisam escrever/alterar

<p style="text-indent: 20px; text-align: justify">
Utilizando o padrão Database-as-a-Service Interface, sempre que um serviço precisar alterar um dado ele deverá fazê-lo mediante uma requisição, no caso podendo ser uma requisição de escrita/leitura. O objetivo de usar esse padrão é diminuir um possível bottleneck que um serviço teria.
</p>

### Bancos individuais

<p style="text-indent: 20px; text-align: justify">
De certo modo, para aumentar a coesão dos serviços é possível que cada serviço possua seu banco interno. Sempre que preciso for o serviço pode conectar-se ao banco público de um outro serviço. Essa abordagem permite separar as lógicas de admnistração para cada serviço.
</p>

#### Relação entre bases de dados diferentes

<p style="text-indent: 20px; text-align: justify">
Pode ser necessário representar e implementar essas relações na camada de modelo de domínio. Ou seja, representar uma relação entre tabelas de dois bancos diferentes. Esse ponto surge quando se pretende utilizar e separar os bancos de dados para cada serviço. Microsserviços não está atrelado a tecnologia, e muitas das tecnologias suportam múltiplas conexões de bancos de dados.
</p>

### Mensageria
<p style="text-indent: 20px; text-align: justify">
Pode ser necessário, em algum momento, utilizar uma abordagem voltada para eventos, ou seja, um serviço notifica os outros de uma determinada alteração importante. Há várias propostas que podem ser usadas para implementar a mensageria entre serviços, como por exemplo, <a href="https://kafka.apache.org/">Apache Kafka</a>.
</p>

### Sugestão de separação
<p style="text-indent: 20px; text-align: justify">
Segue uma lista de possíveis micro serviços e suas responsabilidades:
</p>

- Serviço de Usuários, responsável por toda a parte de autenticação e criação de contas de usuário
- Serviço de Ofertas, responsável por todas as ações relacionadas às ofertas um CRUD para ofertas.
- Serviço de Chat, responsável por lidar com a criação das conversas e das trocas de mensagens entre os usuários
- Serviço de Moderação, contém as lógicas de denúncias de usuário e moderação
- Serviço de Notificação, contém as lógicas de notificação aos clientes, tem funcionamento baseado em eventos e faz uso de mensageria.

<p style="text-indent: 20px; text-align: justify">
Provavelmente, num contexto de um gXchange com muitos usuários, serviços de Usuários, Ofertas e Chat serão um dos que mais vão demandar recursos.
</p>

## Backend For Frontend (BFF)

<p style="text-indent: 20px; text-align: justify">
Com o uso de microsserviços surgiriam vários novos endpoints e muitas vezes em servidores diferentes. Como diminuir o impacto desses serviços para o time de desenvolvimento dos front-ends ou microfrontends?
</p>

<p style="text-indent: 20px; text-align: justify">
Graças o estilo arquitetural Backend for Frontend é possível diminuir esses impactos. A ideia parte do príncipio de criar um único servidor para estes recursos
</p>

![BFF Architecture](https://miro.medium.com/max/1050/1*JTjhbxRxevEfnt4eExWTVw.png)

<p style="text-indent: 20px; text-align: justify">
Cada um desses BFF's são altamente coesos ao seu cliente, a ideia é ser o outro significado do acrônimo, Best Friend, ou seja, melhor amigo de um Front. Essa coesão e esse baixo acoplamento diminui os impactos de mudanças e permite aumento do encapsulamento. Um determinado cliente X não precisa saber da existência de um serviço Y, sendo que ele não faz parte do seu contexto funcionamento.
</p>

<p style="text-indent: 20px; text-align: justify">
Esse padrão funciona bem com a lógica de microfrontends, sendo que a ideia é que o time que mantém um dado microfrontend também mantenha o BFF do mesmo. Facilita também para novos integrantes do time. Não será preciso estudar todos os vários endpoints do Back-end apenas entender o que está disponível no BFF.
</p>

## Referências

> BASS, Len; CLEMENTS, Paul; KAZMAN, Rick. Software Architecture in Practice. 3rd Edition. Addison-Wesley Professional, 2012.

> FOWLER, Martin; JACKSON, Cam. Micro Frontends. 2019. Disponível em: https://martinfowler.com/articles/micro-frontends.html. Acesso em: 30 abr, 2021.

> FOWLER, Martin; LEWIS, James. Microservices Guide. 2019. Disponível em: https://martinfowler.com/microservices/. Acesso em: 30 abr, 2021.

> NEWMAN. Sam. Monolith to Microservices. Chapter 4. Decomposing the Database. Disponível em: https://www.oreilly.com/library/view/monolith-to-microservices/9781492047834/ch04.html. Acesso em: 30 abr, 2021.


## Versionamento
 Versão | Data       | Modificação                    | Motivo | Autor         |
| ------ | ---------- | -------------------------------| ------ | ------------- |
| 1.0 | 30/04/2021 | Criação do documento de arquiteturas alternativas | Documentar as possíveis arquiteturas que poderiam ser utilizadas no gXchange | Todos os integrantes |
| 2.0 | 01/05/2021 | Inclusão do padrão BFF | Incrementar mais ainda as possíveis arquiteturas que poderiam ser usadas | Todos os integrantes |
