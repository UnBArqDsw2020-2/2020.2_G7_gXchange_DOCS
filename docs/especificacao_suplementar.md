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
Não será utilizado nenhum padrão de escrita e/ou notação, será prezada a convenção proposta no <a href="/requisitos/padroes/">documento de padrões dos requisitos</a>.
</p>

### 1.3 Escopo do projeto

<p style="text-indent: 20px; text-align: justify">
O gXchange, assim como já definido anteriormente nos seguintes documentos:
</p>

- [5W2H](/5w2h)
- [Rich picture](/rich_picture)
- [Léxico](/lexico)
- [Requisitos](/requisitos/requisitos/)

### 1.4 Referências

<p style="text-indent: 20px; text-align: justify">
Documentos e recursos utilizados referenciados nesse documento:
</p>

- [Requisitos](/requisitos/requisitos/)
- [Design Sprint](/design_sprint/design_sprint/)

## 2. Descrição geral

### 2.1 Pespectiva de produto

<p style="text-indent: 20px; text-align: justify">
As características de pespectiva do produto podem ser encontradas no <a href="/5w2h/">documento 5W2H</a>.
</p>

### 2.2 Classes e características dos usuários

<p style="text-indent: 20px; text-align: justify">
As características e perfis de usuário estão definidos no <a href="/personas/">documento de personas</a>.
</p>

### 2.3 Ambiente operacional

<p style="text-indent: 20px; text-align: justify">
O ambiente operacional principal do produto serão os navegadores, seja mobile ou web, no caso dos mobiles é pensado o ambiente de PWA (<em>Progressive Web Application</em>), sendo que está pode coexistir com Android e IOS.
</p>

<p style="text-indent: 20px; text-align: justify">
Seguindo os padrões de DevOps tanto o <em>Front-end<em> quanto a API serão fornecidas para executarem dentro de containeres Docker e utilizando o orquestrador de container Docker Compose. Não foi decidido ainda qual servidores hospedarão o aplicativo.
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

## 4. Requisitos de dados

### 4.1 Modelo de dados lógicos

<p style="text-indent: 20px; text-align: justify">
Posteriormente, será definido um diagrama entidade relacionamento. Será utilizado também o <a href="/diagrama_classes/">diagrama de classe</a>.
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
Os atributos de qualidade e seus requisitos estão listados no <a href="/atributos_qualidade/">documento de atributos de qualidade</a>.
</p>

## 7. Requisitos de Internacionalização e Localização

<p style="text-indent: 20px; text-align: justify">
O produto está sendo pensado para a comunidade brasileira de jogadores isso implica a linguagem padrão como sendo português brasieiro.
</p>

## 8. Outros requisitos

## Referências bibliográficas

>WIEGERS, Karl; BEATTY, Joy. "Software Requirements". Microsoft Press, 2013.

## Versionamento

| Versão | Data       | Modificação                    | Motivo | Autor         |
| ------ | ---------- | -------------------------------| ------ | ------------- |
| 1.0 | 05/03/2021 | Criação do documento | Especificar os requisitos não funcionais | Igor Paiva, Rhuan Queiroz, Thiago Guilherme, Thiago Lopes e Washington Bispo |
