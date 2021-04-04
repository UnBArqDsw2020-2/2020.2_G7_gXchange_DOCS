# GRASP

## Introdução

<p style="text-indent: 20px; text-align: justify">
Os principios e padrões GRASP ajudam a entender o essencial de desenho de objetos e aplicar raciocínio de desenho de uma forma metódica, racional, de forma bem explicável. Essa abordagem para o entendimento e uso de princípios de desenho é baseado em padrões de atribuição de responsabilidades (CRAIG, 2004).
</p>

## Palavras-chave

&emsp;[Vendedor](../../../../desenho/base/1.1/lexico/#l7-usuario), [Comprador](../../../../desenho/base/1.1/lexico/#l7-usuario), [Anúncio](../../../../desenho/base/1.1/lexico/#l1-anuncio)

## Discussões entre integrantes

<p style="text-indent: 20px; text-align: justify">
Para a elaboração deste documento foi discutido por várias semanas durante o período da entrega. Algumas dessas discussões estão documentadas nas atas de reuniões. Os pontos principais discutidos foram:
</p>

- Os integrantes haviam pensado na criação do serviço API adapter antes mesmo de estudar GRASPs, e viram posteriormente que o padrão se aplicava.
- Pensamos em como armazenar as fotos de maneira a não deixá-las acopladas às classes que as utilizam (anúncio e usuário), e chegamos a conclusão de que a melhor maneira de fazer isso, seria criando uma model para ela. Dessa forma, teríamos um código mais organizado e manutenível.
- Os integrantes pensaram em criar views para comprador e vendedor, pois por mais que ambos sejam usuários possuem ações diferentes. Para isso foi preciso estudar o padrão arquitetural MVC e MVT para ver se isso não violaria seus princípios. E também foi conversado com a professora para tirar algumas dessas dúvidas (vide [ata dia 22/03](../../../../iniciativa_geral/atas/reuniao_22_03_2021))

## Padrões 

### Creator (Criador)

**Problema:** Quem deve ser responsável por criar uma instância de A? 

**Solução:** Dê a responsabilidade de criação para B, se uma ou mais das situações abaixo for válida.

<ul>
<li><input type="checkbox" style="pointer-events: none"> Se A compõe B</input></li>
<li><input type="checkbox" style="pointer-events: none"> Se B salva A</input></li>
<li><input type="checkbox" style="pointer-events: none"> Se B usa A de forma próxima</input></li>
<li><input type="checkbox" style="pointer-events: none"> Se B possui os dados de inicialização de A</input></li>
</ul>

### Expert (Especialista)

**Problema:** Qual é um princípio geral para atribuir responsabilidades para objetos? 

**Solução:** Dê a responsabilidade para B que contém a informação necessária para satisfazer a responsabilidade.

**Comentário:** No geral, é uma classe especialista em relação a uma classe, pois conhece as informações acerca daquela classe, como também seus métodos, comportamentos e até estados.

### Low Coupling (Baixo acoplamento)

**Problema:** Como suportar baixa dependência, baixo impacto de mudança e aumentar o reúso? 

**Solução:** Atribua responsabilidades para que o acoplamento mantenha-se baixo. Use esse princípio para avaliar as alternativas.

### High Cohesion (Alta Coesão)

**Problema:**  Como manter os objetos focados, entendíveis, gerenciáveis e além disso possuir um baixo um baixo acoplamento?

**Solução:** Atribuir uma responsabilidade de forma a manter a coesão alta.

### Indirection (Indireção)

**Problema:** A quem atribuir a responsabilidade para evitar acoplamento direto entre dois (ou mais) coisas? Como desacoplar objetos para que o baixo acoplamento seja suportado e o reúso se mantenha potencialmente alto?

**Solução:** Dê a responsabilidade para um objeto intermediário entre os componenetes ou serviços de forma que eles não estejam diretamente acoplados.

### Protected Variations (Variações Protegidas)

**Problema:** Como desenhar objetos, subsistemas e sistemas para que variações ou instabilidades nesses elementos, não tenham um impacto indesejado em outros elementos 

**Solução:** Identifique pontos de variações ou instabilidades previstas, atribua responsabilidades para criar uma interface (no sentido geral) estável em volta destes pontos;

## Casos Aplicados

### Chat e Mensagem

GRASPs:

- Criador
- Especialista

<p style="text-indent: 20px; text-align: justify">
Visto que a relação entre Chat e Mensagem se encaixam em todos os critérios estabelicidos para criador
</p>

<ul>
<li><input type="checkbox" checked style="pointer-events: none"> Se Mensagem compõe Chat</input></li>
<li><input type="checkbox" checked style="pointer-events: none"> Se Chat salva Mensagem</input></li>
<li><input type="checkbox" checked style="pointer-events: none"> Se Chat usa Mensagem de forma próxima</input></li>
<li><input type="checkbox" checked style="pointer-events: none"> Se Chat possui os dados de inicialização de Chat</input></li>
</ul>

<p style="text-indent: 20px; text-align: justify">
Além do mais, o Chat possui todas as informações que compõem as mensagens, no caso o contéudo e quando ela foi enviada, ele receberá a responsabilidade de não somente criar, mas também salvar e recuperar as mensagens, tornando-o assim num especialista de informações das Mensagens. 
</p>

### Usuário e anúncio

GRASPs:

- Criador

<p style="text-indent: 20px; text-align: justify">
Visto que a relação entre Usuário e Anúncio se encaixam em alguns dos critérios citados acima, mas principalmente por deter dos dados iniciais e da responsabilidade de salvar o anúncio.
</p>

<ul>
<li><input type="checkbox" style="pointer-events: none"> Se Anúncio compõe Usuário</input></li>
<li><input type="checkbox" checked style="pointer-events: none"> Se Usuário salva Anúncio</input></li>
<li><input type="checkbox" style="pointer-events: none"> Se Usuário usa Anúncio de forma próxima</input></li>
<li><input type="checkbox" checked style="pointer-events: none"> Se Usuário possui os dados de inicialização de Anúncio</input></li>
</ul>

### Serializers

GRASPs:

- Especialista
- Criador (quando aplicável)

<p style="text-indent: 20px; text-align: justify">
As Serializers do padrão django-rest podem ser consideradas especialistas em uma ou mais models dada uma necessidade e um tipo de informação. Além do mais algumas delas são as responsáveis por criar novas instâncias das models e salvá-las na camada de persistência.
</p>

#### PersonSerializer cria Person e User

<p style="text-indent: 20px; text-align: justify">
Visto que há uma especialização de Pessoa (Person) e Usuário (User) é conveniente que o usuário seja iniciado vazio. A classe PersonSerializer, no back-end, tem a responsabilidade de criar tanto a Model Person com os dados de Pessoa e a Model User como especialização. Vale lembrar também que a Model User não possui dados de inicialização além da chave de especialização.
</p>

<ul>
<li><input type="checkbox" style="pointer-events: none"> Se Person e ser compõe PersonSerializer </input></li>
<li><input type="checkbox" checked style="pointer-events: none"> Se PersonSerializer salva Person e User</input></li>
<li><input type="checkbox" checked style="pointer-events: none"> Se PersonSerializer usa Person e User de forma próxima</input></li>
<li><input type="checkbox" checked style="pointer-events: none"> Se PersonSerializer possui os dados de inicialização de Person e User</input></li>
</ul>

### Anúncio E Foto

GRASPs:

- Low-coupling
- Alta Coesão
- Variações protegidas 

<p style="text-indent: 20px; text-align: justify">
Ter uma model de fotos permite que as fotos sejam desacopladas da model de anúncio e estabelecidas como uma associação. Desse modo o componente Foto pode possuir suas próprias regras de funcionamento. 
</p>

<p style="text-indent: 20px; text-align: justify">
Suponha uma situação em que você precise trocar o sistema, no caso qual módulo vai servir as fotos, no caso trocar do armazamento de estáticos (imagens e afins) da AWS para um servidor próprio Apache ou Nginx. As regras de upload e obtenção da URL vai permanecer sendo responsabilidade do componente Foto. Desse modo diminui o efeito de mudanças nas regras de Foto. 
</p>

### Api handler (API Adapter) sabe como conversar com a API

GRASPs:

- Indirection
- Alta coesão
- Variações protegidas

<p style="text-indent: 20px; text-align: justify">
É uma indireção pois é um componente para lidar com a conversa entre os componentes do front-end e a API. Isso fornece uma maior coesão, pois os componentes do front-end não precisam implementar a lógica de conversa com a API, mantendo-se apenas nas suas próprias responsabilidades.
</p>

<p style="text-indent: 20px; text-align: justify">
Dessa forma é criado o API Adapter que é uma classe que possui uma instância privada do Axios além dos verbos HTTP (biblioteca usada para requisições HTTP em Javascript), essa instância só pode ser acessada dentro da classe protegendo-a de mudanças externas.
</p>

### Django Views

GRASPs:

- Polimorfismo
- Indirection
- High Cohesion

#### BuyerView

<p style="text-indent: 20px; text-align: justify">
A ideia é que a View de Buyer (Comprador) seja responsável pelas ações relacionadas ao comprador.
</p>

#### SellerView

<p style="text-indent: 20px; text-align: justify">
A ideia é que a View de Seller (Vendedor) seja responsável pelas ações relacioadas ao vendedor.
</p>

### Pacotes front-end

GRASPs:

- Low Coupling
- High Cohesion

#### Pacote de services

<p style="text-indent: 20px; text-align: justify">
Esse pacote de <em>services</em>, no Front-end, vai conter serviços comuns que são utilizados por diversos componentes, por exemplo, a API Adapter está na pacote de services e outras funcionalidades podem vir a ser adicionas.
</p>

#### Pacote de utils

<p style="text-indent: 20px; text-align: justify">
Esse pacote de <em>utils</em>, no Front-end, vai conter utilidades comuns que são usadas por vários componentes, por exemplo, <em>parse</em> de datas e horas.
</p>

## Referências

> CRAIG. Larman. "Applying UML and Patterns: An Introduction to Object-Oriented Analysis and Design and Iterative Development". Prentice Hall. Pearson 2005.

## Versionamento

| Versão | Data       | Modificação               | Motivo | Autor         |
| ------ | ---------- | ------------------------- | ------ | ------------- |
|  1.0   | 04/04/2021 | Criação do documento | - | Todos os integrantes |
