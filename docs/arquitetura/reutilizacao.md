# Documento de reutilização

## Propósito

<p style="text-indent: 20px; text-align: justify">
Este documento tem como propósito evidenciar os pontos de reutilização que já estão disponíveis e poderão estar no desenvolvimento do gXchange
</p>

## Implantação

<p style="text-indent: 20px; text-align: justify">
No contexto de implantação, e seguinto o conceito de infraestrutura como código, em ambos os repositórios, tanto de back-end quanto de front-end contém uma estrutura padrão que podem ser utilizadas para conteinerizar aplicações React e Django + Postgresql.
</p>

### Front-end

<p style="text-indent: 20px; text-align: justify">
Para a criação do segundo front-end a estrutura base do conteiner React dockerizado (Docker + docker-compose) pode ser encontrado nos seguintes arquivos:
</p>

- [Dockerfile](https://github.com/UnBArqDsw2020-2/2020.2_G7_gXchange_Frontend/blob/develop/Dockerfile)
- [docker-compose](https://github.com/UnBArqDsw2020-2/2020.2_G7_gXchange_Frontend/blob/develop/docker-compose.yml)

<p style="text-indent: 20px; text-align: justify">
De modo semelhante, é possível utilizar as funcionalidades do Git para clonar a estrutura base do Front-end para ser utilizado no Front-end de Moderador, e também serve até para outros Front-end baseados em React. É possível criar um boilerplate seguindo a mesma lógica.
</p>

### Back-end

<p style="text-indent: 20px; text-align: justify">
Para a criação de um conteiner Django com banco de dados Postgresql os arquivos de configuração do Docker podem ser utilizados:
</p>

- [Dockerfile](https://github.com/UnBArqDsw2020-2/2020.2_G7_gXchange_Backend/blob/develop/Dockerfile)
- [docker-compose](https://github.com/UnBArqDsw2020-2/2020.2_G7_gXchange_Backend/blob/develop/docker-compose.yaml)

## Componentes da folha de estilo

<p style="text-indent: 20px; text-align: justify">
No contexto de padronização e reutilização de componentes nos front-end é interessante empacotar todos os componentes reusáveis do sistema, dessa forma o código de ambos ficaria mais coesos implementariam o padrão definido. Isso também aumenta a manutenibilidade do sistema, visto que a mudança no pacote já seria refletida nos sistemas que o utilizam.
</p>

<p style="text-indent: 20px; text-align: justify">
Do modo que foi proposto, o estado interno dos componentes e toda a sua lógica interna e parte da lógica de estilização são considerados FrozenSpots.
</p>

## Services e Utils (Front-End)

<p style="text-indent: 20px; text-align: justify">
Quase todas as funcionalidades presentes no pacote de <em><strong>utils</strong></em> podem ser reutilizadas, visto que fornecem funcionalidades genéricas e também utilidades no contexto do sistema, que podem ser necessárias em outros módulos.
</p>

### API Adapter

<p style="text-indent: 20px; text-align: justify">
A porção de código referente a classe API Adapter pode ser utilizada em qualquer projeto que utilize Typescript e autenticação baseada em JWT (com algumas alterações é possível utilizar outros meios de autenticação). Com algumas alterações em relação ao ambiente, URL da API e TIMEOUT.
</p>

O código pode ser encontrado [aqui](https://github.com/UnBArqDsw2020-2/2020.2_G7_gXchange_Frontend/blob/develop/src/services/api.ts).

### Token e Local Storage

<p style="text-indent: 20px; text-align: justify">
O pacote <em><strong>auth</strong></em> contém funções que são úteis para controlar os <em>Tokens</em> de autenticação no Front-end. Pode ser exportado como um pacote e compartilhado com outros Front-ends.
</p>

O pacote pode ser encontrado [aqui](https://github.com/UnBArqDsw2020-2/2020.2_G7_gXchange_Frontend/blob/develop/src/services/auth.ts).

### Base64 Codificação e Decodificação

<p style="text-indent: 20px; text-align: justify">
Foi tomada a decisão de utilizar e armazenar as imagens no formato binário, então a interface de comunicação de binários do Cliente e Servidor tornou-se o Base64. O pacote images em utils, possui métodos que conseguem Codificar e Decodificar imagens para o padrão base64.
</p>

O pacote pode ser encontrado [aqui](https://github.com/UnBArqDsw2020-2/2020.2_G7_gXchange_Frontend/blob/develop/src/utils/images/index.ts).

### Compressão de imagens

<p style="text-indent: 20px; text-align: justify">
O módulo de compressão e descompressão de imagens também é passível de reutilização visto que qualquer tipo de imagem já irá ser convertida, por padrão, para o modelo do sistema (que pode ser alterado facilmente se necessário).
</p>

<p style="text-indent: 20px; text-align: justify">
Pode ser considerado um HotSpot pois os paramêtros de compressão podem ser trocados de maneira simples.
</p>

O pacote pode ser encontrado [aqui](https://github.com/UnBArqDsw2020-2/2020.2_G7_gXchange_Frontend/blob/develop/src/utils/images/index.ts).

## Django Apps

<p style="text-indent: 20px; text-align: justify">
Tomando a arquitetura monolítica do gXchange - API, o Framework Django permite que, sejam criados outros apps dentro de uma mesma API, o conceito de app do Django segue a ideia de um mini projeto com sua própria estrutura MVT.
</p>

<p style="text-indent: 20px; text-align: justify">
Neste mesmo contexto, caso seja necessário criar um app com outro próposito mantendo assim a coesão. É possível utilizar as classes do modelo de domínio, sem a necessidade de duplicar ou reimplementar as models que serão necessárias.
</p>

<p style="text-indent: 20px; text-align: justify">
Deste modo é possível amenizar os efeitos negativos de uma arquitetura monolítica.
</p>

[Leia mais sobre Django APPs](https://docs.djangoproject.com/)

## Django JWT Logged user

<p style="text-indent: 20px; text-align: justify">
No pacote de utils da gXchange API há duas funcionalidades que podem ser reutilizáveis que são a de obter usuário logado e obter o email do usuário logado. Estas funcionalidades decodificam o token JWT do usuário para obter suas informações, esssas podem ser utilizadas pelas <em>views</em> e <em>serializers</em> para realizarem tarefas relacionadas ao usuário logado.
</p>

## WebSocket

<p style="text-indent: 20px; text-align: justify">
A modelagem arquitetural proposta no <a href="../padroes/das/#514-notificacoes">DAS</a> para criar um serviço de notificações pode ser utilizada em outras relações cliente-servidor que queiram utilizar WebSocket. Até pode ser agregado em outras arquiteturas. A modelagem em si é um frozenSpot, mas como cabe ao utilizador definir como implementar, reside um HotSpot.
</p>

## Referências

> MIRANDA JUNIOR, Pasteur. Frameworks. Disponível em: https://www.tesestec.com.br/pasteurjr/Frameworks.pdf. Acesso em: 30 abr, 2021.

> VERGILIO, Silvia. Padrões Arquiteturais. Disponível em: https://www.inf.ufpr.br/andrey/ci163/PadroesFrameworksAl.pdf. Acesso em: 30 abr, 2021.

> MARKIEWICZ, Marcus E; LUCENA, Carlos. Understanding Object-Oriented Framework Engineering. PUC-Rio. Disponível em: http://www.dbd.puc-rio.br/depto_informatica/00_38_markiewicz.pdf. Acesso em: 30 abr, 2021.

## Versionamento

| Versão | Data | Modificação  | Motivo  | Autor  |
| ------ | ---------- | --- | ------ | ------ |
| 1.0    | 30/04/2021 | Criação do documento  | Listar as partes orientadas ao reúso | Todos os integrantes |
