# Especificação dos requisitos 

## 1. Introdução

<p style="text-indent: 20px; text-align: justify">
A organização desse documento baseia-se no padrão proposto por Wiegers e Beatty (2013)
</p>

### 1.1 Propósito

<p style="text-indent: 20px; text-align: justify">
A especificação dos requisitos aborda os requisitos funcionais e principalmente os não funcionais do sistema, basicamente se aliando com outras técnicas de requisitos como a modelagem e a elicitação possibilitando ter uma margem mais robusta de alcançar os requisitos do sistema.
</p>

### 1.2 Convenções do documento

<p style="text-indent: 20px; text-align: justify">
Não será utilizado nenhum padrão de escrita e/ou notação, será prezada a convenção proposta no <a href="/desenho/base/1.1/requisitos/padroes/">documento de padrões dos requisitos</a>.
</p>

### 1.3 Escopo do projeto

<p style="text-indent: 20px; text-align: justify">
O gXchange, assim como já definido anteriormente nos seguintes documentos:
</p>

- [5W2H](/desenho/base/1.1/5w2h)
- [Rich picture](/desenho/base/1.1/rich_picture)
- [Léxico](/desenho/base/1.1/lexico)
- [Requisitos](/desenho/base/1.1/requisitos/requisitos/)

### 1.4 Referências

<p style="text-indent: 20px; text-align: justify">
Documentos e recursos utilizados referenciados nesse documento:
</p>

- [Requisitos](/desenho/base/1.1/requisitos/requisitos/)
- [Design Sprint](/desenho/base/1.1/design_sprint/design_sprint/)

## 2. Descrição geral

### 2.1 Pespectiva de produto

<p style="text-indent: 20px; text-align: justify">
As características de pespectiva do produto podem ser encontradas no <a href="/desenho/base/1.1/5w2h/">documento 5W2H</a>.
</p>

### 2.2 Classes e características dos usuários

<p style="text-indent: 20px; text-align: justify">
As características e perfis de usuário estão definidos no <a href="/desenho/base/1.1/personas/">documento de personas</a>.
</p>

### 2.3 Ambiente operacional

<p style="text-indent: 20px; text-align: justify">
O ambiente operacional principal do produto serão os navegadores, seja mobile ou web, no caso dos mobiles é pensado o ambiente de PWA (<em>Progressive Web Application</em>), sendo que está pode coexistir com Android e IOS.
</p>

<p style="text-indent: 20px; text-align: justify">
Seguindo os padrões de DevOps tanto o <em>Front-end</em> quanto a API serão fornecidas para executarem dentro de containeres <em>Docker</em> e utilizando o orquestrador de container Docker Compose. Não foi decidido ainda qual servidores hospedarão o aplicativo.
</p>
 

### 2.4 Limitações de design e implementação

<p style="text-indent: 20px; text-align: justify">
Dada as condições e o conhecimento dos integrantes as linguagens de programação que serão utilizadas são: Typescript e Python, utilizando React e Django como respectivos <em>frameworks</em>.
</p>

<p style="text-indent: 20px; text-align: justify">
Será utilizada a biblioteca <a href="https://material-ui.com/" target="_blank" rel="noopenner">material-ui/core</a> para a padronização dos componentes e seu reuso. Será utilizada também para realização de requisições a biblioteca <a href="https://github.com/axios/axios" target="_blank" rel="noopenner">Axios</a>
</p>

<p style="text-indent: 20px; text-align: justify">
Para o contexto da API no <em>back-end</em>, será utilizado o <em>Django REST framework</em> e o pacote <em>REST framework JWT Auth</em>.
</p>

### 2.5 Dependências e suposições

<p style="text-indent: 20px; text-align: justify">
Para o sistema de email, será utilizado o sendgrip. 
</p>

## 3. Funcionalidades do Sistema

<p style="text-indent: 20px; text-align: justify">
Será convencionado os graus de granularidade do sistema como sendo:
</p>

- User Story (História de usuário): algo que pode ser desenvolvido em uma iteração (Sprint)
- Epic (Épico): pode ser um conjunto de histórias de usuário ou um conjunto de épicos menores
- Feature (funcionalidade): Grupo de capacidades do sistema que agregam valor ao usuário. Seja: 
    - Uma história de usuário
    - Um conjunto de histórias de usuário
    - Um épico
    - Um conjunto de épicos

### 3.1 Controle de conta

#### 3.1.1 Descrição

<p style="text-indent: 20px; text-align: justify">
O usuário deve ser capaz de criar uma conta, editar as informações pessoais, desativar ou excluir a sua conta. Além de poder realizar login no sistema utilizando suas credenciais. Possui prioridade Alta.
</p>

#### 3.1.2 Requisitos funcionais

- RF-01
- RF-02
- RF-03
- RF-24
- RF-25
- RF-29
- RF-30
- RF-31

### 3.2 Controle de anúncios

#### 3.2.1 Descrição

<p style="text-indent: 20px; text-align: justify">
O usuário, como vendedor, deve ser capaz de criar um anúncio, editar suas informações, excluir o anúncio e visualizar todos seus anúncios. Possui prioridade Alta.
</p>

#### 3.2.2 Requisitos funcionais

- RF-08
- RF-12
- RF-19
- RF-20
- RF-39

### 3.3 Feed de anúncios

#### 3.3.1 Descrição

<p style="text-indent: 20px; text-align: justify">
O usuário deve ser capaz de acessar, visualizar e filtrar o feed contendo os anúncios disponíveis e também visualizar um anúncio específico. Possui prioridade Alta.
</p>

#### 3.3.2 Requisitos funcionais

- RF-07
- RF-17
- RF-26
- RF-27
- RF-28
- RF-36

### 3.4 Perfil de usuário

#### 3.4.1 Descrição

<p style="text-indent: 20px; text-align: justify">
O usuário deve ser capaz de visualizar o perfil de outros usuários. Possui prioridade Média.
</p>

#### 3.4.2 Requisitos funcionais

- RF-33

### 3.5 Avaliação de usuário

#### 3.5.1 Descrição

<p style="text-indent: 20px; text-align: justify">
Um usuário, seja vendedor ou comprador, após a interação, deve ser capaz de avaliar o outro usuário envolvido. Possui prioridade Média.
</p>

#### 3.5.2 Requisitos funcionais

- RF-05
- RF-06
- RF-41

### 3.6 Denúncias do usuário

#### 3.6.1 Descrição

<p style="text-indent: 20px; text-align: justify">
Um usuário, seja vendedor ou comprador, após a interação, deve ser capaz de reportar o outro usuário envolvido ou o anúncio em questão. Possui prioridade Média.
</p>

#### 3.6.2 Requisitos funcionais

- RF-04
- RF-09
- RF-10
- RF-13
- RF-14

### 3.7 Moderador do sistema

#### 3.7.1 Descrição

<p style="text-indent: 20px; text-align: justify">
Um usuário, como moderador, deve ser capaz de visualizar, remover denúncias, deve ser capaz de invalidar, validar e excluir anúncio, deve ser capaz de banir usuários. Possui prioridade Baixa.
</p>

#### 3.7.2 Requisitos funcionais

- RF-15
- RF-22
- RF-23
- RF-34

### 3.7 Notificar usuário

#### 3.7.1 Descrição

<p style="text-indent: 20px; text-align: justify">
Um vendedor deve ser notificado das alterações de estado dos seus anúncios e de mensagens recebidas, um comprador deve ser notificado quando o anúncio que ele reportou foi invalidado. Possui prioridade Baixa.
</p>

#### 3.7.2 Requisitos funcionais

- RF-16
- RF-18
- RF-21

### 3.8 Chat de usuários

#### 3.8.1 Descrição

<p style="text-indent: 20px; text-align: justify">
Um usuário, como comprador, deve ser capaz de enviar mensagens para um vendedor por meio de um anúncio, visualizar as mensagens enviadas e receber mensagens. Um usuário, como vendedor, deve ser capaz de visualizar os chats de anúncios e as conversas de cada chat. Possui prioridade Alta.
</p>

#### 3.8.2 Requisitos funcionais

- RF-11
- RF-35

### 3.9 Qualidade de mídia

#### 3.9.1 Descrição

<p style="text-indent: 20px; text-align: justify">
Um usuário deve ser garantido pelo sistema que a qualidade das mídias de um anúncio são boas. Possui prioridade baixíssima.
</p>

#### 3.9.2 Requisitos funcionais

- RF-37
- RF-38

### 3.10 Login por impressão digital

#### 3.10.1 Descrição

<p style="text-indent: 20px; text-align: justify">
Um usuário deve ser capaz de realizar login utilizando a impressão digital. Possui prioridade baixíssima.
</p>

#### 3.10.2 Requisitos funcionais

- RF-32

### 3.11 Ajuda e suporte

#### 3.11.1 Descrição

<p style="text-indent: 20px; text-align: justify">
Um usuário deve ser capaz de acessar a seção de ajuda e suporte do sistema. Possui prioridade baixa.
</p>

#### 3.11.2 Requisitos funcionais

- RF-40

## 4. Requisitos de dados

### 4.1 Modelo de dados lógicos

<p style="text-indent: 20px; text-align: justify">
Posteriormente, será definido um diagrama entidade relacionamento. Será utilizado também o <a href="/desenho/modelage/2.1/diagrama_classes/">diagrama de classe</a>.
</p>

### 4.2 Dicionário de dados

<p style="text-indent: 20px; text-align: justify">
Posteriormente, será definido um dicionário de dados. 
</p>

### 4.3 Relatórios

<p style="text-indent: 20px; text-align: justify">
No momento, não há propósito de extrair relatórios da aplicação. 
</p>

### 4.4 Aquisição, integridade, retenção e disposição dos dados

<p style="text-indent: 20px; text-align: justify">
Os dados serão obtidos diretamente do usuário, por meio da aplicação. Os mesmos serão mantidos na base de dados de um sistema gerenciador de banco de dados (SGBD). A integridade dos dados é de responsabilidade do SGBD. Os dados serão dispostos pela API <strong>somente</strong> para uso dentro do contexto da aplicação. Não há pretensão de realizar <em>backup</em> desses dados.
</p>

## 5. Requisitos de interface externa

<p style="text-indent: 20px; text-align: justify">
Esta seção refere-se aos requisitos de interface que os componentes sejam de software ou não precisam para que aconteça a comunicação.
</p>

### 5.1 Interface do usuário

<p style="text-indent: 20px; text-align: justify">
Será criado um documento que serve como guia de estilos posteriormente.
</p>

### 5.2 Interfaces de software

<p style="text-indent: 20px; text-align: justify">
A comunicação com o banco de dados é abstraída pelo Django. Enquanto que o padrão de comunicação, por meio de requisições, será o padrão de requisições JSON.
</p>

<p style="text-indent: 20px; text-align: justify">
Outras interfaces de software, estados e comunicações podem ser visualizadas nos diagramas UML da aba de modelagem.
</p>

### 5.3 Interfaces de hardware

<p style="text-indent: 20px; text-align: justify">
O sistema não depende de nenhum hardware externo.
</p>

### 5.4 Interfaces de software

<p style="text-indent: 20px; text-align: justify">
Para o sistema de email, deverá ser utilizado o sistema sendgrip com a restrição de 100 emails por dia.
</p>

<p style="text-indent: 20px; text-align: justify">
Sobre o protocolo de rede, será utilizado o smtp para email e o https como protocolo de rede. 
</p>

## 6. Atributos de qualidade

<p style="text-indent: 20px; text-align: justify">
Os atributos de qualidade e seus requisitos estão listados no <a href="/desenho/modelagem/iniciativa/atributos_qualidade/">documento de atributos de qualidade</a>.
</p>

## 7. Requisitos de Internacionalização e Localização

<p style="text-indent: 20px; text-align: justify">
O produto está sendo pensado para a comunidade brasileira de jogadores isso implica a linguagem padrão como sendo português brasieiro.
</p>

## Referências bibliográficas

>WIEGERS, Karl; BEATTY, Joy. "Software Requirements". Microsoft Press, 2013.

## Versionamento

| Versão | Data       | Modificação                    | Motivo | Autor         |
| ------ | ---------- | -------------------------------| ------ | ------------- |
| 1.0 | 05/03/2021 | Criação do documento | Especificar os requisitos não funcionais | Igor Paiva, Rhuan Queiroz, Thiago Guilherme, Thiago Lopes e Washington Bispo |
