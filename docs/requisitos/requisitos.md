# Requisitos

## Introdução

<p style="text-indent: 20px; text-align: justify">
Este documento lista todos os requisitos elicitados, informando suas respectivas técnicas, priorização e identificação única.
</p>

## Técnica de priorização

<p style="text-indent: 20px; text-align: justify">
Para a priorização será utilizada o método MoSCoW.
</p>

<p style="text-indent: 20px; text-align: justify">
MoSCoW é uma técnica que busca priorizar os requisitos a partir de escalas, tendo como vantagem sua simplicidade quando comparada com outras técnicas, possibilitanto priorizar cada requisito elicitado para o projeto. O MoSCoW classifica os requisitos em 4 escalas:
</p>

- **Must**: o requisito deve ser satisfeito para que a solução seja considerada um sucesso.
- **Should**: o requisito é importante e deve ser incluído na solução se possível, mas não é obrigatório para o sucesso.
- **Could**: é um requisito desejado, mas um que pode ser satisfeito ou eliminado. Deve ser implementado apenas se houver tempo e recurso.
- **Won't**: é um requisito que não será implementado, mas pode ser incluída em uma futura *release* ou nem ser implementada.

## Requisitos Elicitados

### Legenda
Legenda aplicável à rastreabilidade:

- BTipo-número
    - Refere-se ao número do requisito no [Documento de Brainstorming](/requisitos/brainstorming/)
    - Tipo: F para requisitos funcionais, NF para requisitos não funcionais
    - Exemplo: BF-4 Refere-se ao requisito funcional de número 4. BNF-2 Refere-se ao requisito não funcional de número 2.
- ITipo-número
    - Refere-se ao número do requisito no [Documento de Introspecção](/requisitos/introspeccao/)
    - Tipo: F para requisitos funcionais, NF para requisitos não funcionais
    - Exemplo: IF-1 Refere-se ao requisito funcional de número 1 do [Documento de Introspecção](/requisitos/introspeccao/), INF-1 Refere-se ao requisito não funcional de número 1 do [documento de Introspecção](/requisitos/introspeccao/)
- QTipo-número
    - Refere-se ao número do requisito no [Documento de Questionário](/requisitos/questionario/)
    - Tipo: F para requisitos funcionais, NF para requisitos não funcionais
    - Exemplo: QF-4 Refere-se ao requisito funcional de número 4 do documento de [Questionário](/requisitos/questionario/). QNF-2 Refere-se ao requisito não funcional de número 2 do [Documento de Questionário](/requisitos/questionario/).

### Funcionais

| Identificador | Requisito | Prioridade | Rastreabilidade |
|:--:|--|:--:|:--:|
| RF-01 | O [vendedor](/lexico/#l7-usuario) e [comprador](/lexico/#l7-usuario) devem ser capazes de se cadastrarem usando sua conta do Google | **Should** | [IF-1](/requisitos/introspeccao/#requisitos), [BF-3](/requisitos/brainstorming/#requisitos), [QF-10](/requisitos/questionario/#funcionais) |
| RF-02 | O [vendedor](/lexico/#l7-usuario) e [comprador](/lexico/#l7-usuario) devem ser capazes de se cadastrarem usando sua conta do Facebook | **Should** |[IF-2](/requisitos/introspeccao/#requisitos), [BF-2](/requisitos/brainstorming/#requisitos), [QF-9](/requisitos/questionario/#funcionais) |
| RF-03 | O [vendedor](/lexico/#l7-usuario) e [comprador](/lexico/#l7-usuario) devem ser capazes de criarem uma conta do sistema utilizando seu e-mail | **Must** | [IF-3](/requisitos/introspeccao/#requisitos), [BF-1](/requisitos/brainstorming/#funcionais), [QF-8](/requisitos/questionario/#funcionais) |
| RF-04 | O [comprador](/lexico/#l7-usuario) deve ser capaz de [reportar](/lexico/#l6-reportar) um [anúncio](/lexico/#l1-anuncio) feito por um [vendedor](/lexico/#l7-usuario)|  **Must** |  [IF-4](/requisitos/introspeccao/#requisitos) 
| RF-05 | O [comprador](/lexico/#l7-usuario) deve ser capaz de [avaliar](/lexico/#l5-avaliar) um [vendedor](/lexico/#l7-usuario) após realizar uma [troca](/lexico/#l3-trocar) ou [venda](/lexico/#l2-vender) | **Must** | [IF-5](/requisitos/introspeccao/#requisitos), [BF-8](/requisitos/brainstorming/#funcionais) e [QF-4](/requisitos/questionario/#funcionais) |
| RF-06 | O [vendedor](/lexico/#l7-usuario) deve ser capaz de [avaliar](/lexico/#l5-avaliar) um [comprador](/lexico/#l7-usuario) após a realização de uma [venda](/lexico/#l2-vender) ou [troca](/lexico/#l3-trocar) | **Must** | [IF-6](/requisitos/introspeccao/#requisitos), [BF-9](/requisitos/brainstorming/#funcionais) e [QF-4](/requisitos/questionario/#funcionais) |
| RF-07 | O [comprador](/lexico/#l7-usuario) deve ser capaz de visualizar as informações dos [anúncios](/lexico/#l1-anuncio) | **Must** | [IF-7](/requisitos/introspeccao/#requisitos), [BF-17](/requisitos/brainstorming/#requisitos), [QF-1](/requisitos/questionario/#funcionais) e [QF-12](/requisitos/questionario/#funcionais) |
| RF-08 | O [vendedor](/lexico/#l7-usuario) deve ser capaz de cadastrar um novo [anúncio](/lexico/#l1-anuncio) | **Must** | [IF-8](/requisitos/introspeccao/#requisitos), [BF-11](/requisitos/brainstorming/#funcionais) |
| RF-09 | O [comprador](/lexico/#l7-usuario), após ter interagido com [vendedor](/lexico/#l7-usuario), deve ser capaz de [reportar](/lexico/#l6-reportar) o [vendedor](/lexico/#l7-usuario) | **Must** | [IF-9](/requisitos/introspeccao/#requisitos), [BF-10](/requisitos/brainstorming/#requisitos) |
| RF-10 | O [vendedor](/lexico/#l7-usuario), após ter interagido com [comprador](/lexico/#l7-usuario), deve ser capaz de [reportar](/lexico/#l6-reportar) o [comprador](/lexico/#l7-usuario) | **Must** | [IF-10](/requisitos/introspeccao/#requisitos) |
| RF-11 | O sistema deve fornecer um sistema de mensagens para o [comprador](/lexico/#l7-usuario) e o [vendedor](/lexico/#l7-usuario) interagirem | **Should** | [IF-11](/requisitos/introspeccao/#requisitos), [BF-14](/requisitos/brainstorming/#requisitos) e [QF-2](/requisitos/questionario/#funcionais) |
| RF-12 | O sistema deve salvar um [anúncio](/lexico/#l1-anuncio) com as seguintes características: nome do(s) [jogo(s)](/lexico/#l4-jogo), plataforma, condição, foto(s), informações do [vendedor](/lexico/#l7-usuario), localização, preço e descrição | **Must** | [IF-12](/requisitos/introspeccao/#requisitos), [BF-12](/requisitos/brainstorming/#funcionais) |
| RF-13 | O sistema deve persistir as mensagens entre o [comprador](/lexico/#l7-usuario) e [vendedor](/lexico/#l7-usuario) de um determinado [anúncio](/lexico/#l1-anuncio) por 7 dias após o fechamento desse [anúncio](/lexico/#l1-anuncio), contanto que não haja nenhuma denúncia do [comprador](/lexico/#l7-usuario) ou [vendedor](/lexico/#l7-usuario). Nesse caso, as mensagens deverão ser mantidas até a resolução da denúncia. | **Should** | [IF-13](/requisitos/introspeccao/#requisitos) |
| RF-14 | O sistema deve manter as mensagens entre o [comprador](/lexico/#l7-usuario) e [vendedor](/lexico/#l7-usuario) disponíveis para que elas possam ser avaliadas, por moderadores, no caso de denúncias | **Should** | [IF-14](/requisitos/introspeccao/#requisitos) |
| RF-15 | O moderador deve ser capaz de [invalidar](/lexico/#l8-invalidar) um [anúncio](/lexico/#l1-anuncio) | **Could** | [IF-15](/requisitos/introspeccao/#requisitos) |
| RF-16 | O sistema deverá notificar o [vendedor](/lexico/#l7-usuario) caso seu [anúncio](/lexico/#l1-anuncio) seja [invalidado](/lexico/#l8-invalidar) | **Could** | [IF-16](/requisitos/introspeccao/#requisitos) |
| RF-17 | O sistema deve listar apenas [anúncios válidos](/lexico/#l9-anuncio-valido) | **Could** | [IF-17](/requisitos/introspeccao/#requisitos) |
| RF-18 | O sistema deverá notificar o [usuário](/lexico/#l7-usuario) quando um [anúncio](/lexico/#l1-anuncio) que ele reportou for [invalidado](/lexico/#l8-invalidar) | **Could** | [IF-18](/requisitos/introspeccao/#requisitos) |
| RF-19 | O [vendedor](/lexico/#l7-usuario) deve ser capaz de remover um [anúncio](/lexico/#l1-anuncio) | **Must** | [IF-19](/requisitos/introspeccao/#requisitos) |
| RF-20 | O [vendedor](/lexico/#l7-usuario) deve ser capaz de editar um anúncio | **Must** | [IF-20](/requisitos/introspeccao/#requisitos) |
| RF-21 | O sistema deve notificar o [comprador](/lexico/#l7-usuario) e [vendedor](/lexico/#l7-usuario) de novas mensagens | **Should** | [IF-21](/requisitos/introspeccao/#requisitos) |
| RF-22 | O [moderador](/lexico/#l7-usuario) deve ser capaz de visualizar as denúncias de [anúncios](/lexico/#l1-anuncio), [vendedores](/lexico/#l7-usuario) e O [compradores](/lexico/#l7-usuario) | **Could** | [IF-22](/requisitos/introspeccao/#requisitos) |
| RF-23 | O [moderador](/lexico/#l7-usuario) deve ser capaz de banir um [usuário](/lexico/#l7-usuario) [**(a ser decidido)**](/requisitos/padroes/#a-ser-decidido) | **Could** | [IF-23](/requisitos/introspeccao/#requisitos), [BF-15](/requisitos/brainstorming/#requisitos) |
| RF-24 | O sistema no momento de cadastro, deve pedir o consentimento dos [usuários](/lexico/#l7-usuario) em relação aos termos de uso [**(a ser decidido)**](/requisitos/padroes/#a-ser-decidido) | **Must** | [IF-24](/requisitos/introspeccao/#requisitos) |
| RF-25 | O sistema deve salvar [usuários](/lexico/#l7-usuario) com as seguintes características: nome, apelido (nome de [usuário](/lexico/#l7-usuario)), email e senha | **Must** | [IF-25](/requisitos/introspeccao/#requisitos) |
| RF-26 | O [comprador](/lexico/#l7-usuario) deve ser capaz de visualizar todos os [anúncios válidos](/lexico/#l9-anuncio-valido) cadastrados | **Could** | [IF-26](/requisitos/introspeccao/#requisitos) |
| RF-27 | O [comprador](/lexico/#l7-usuario) deve ser capaz de filtrar os [anúncios](/lexico/#l1-anuncio) por suas informações | **Should** | [IF-27](/requisitos/introspeccao/#requisitos), [BF-18](/requisitos/brainstorming/#funcionais), [QF-7](/requisitos/questionario/#funcionais) |
| RF-28 | O [comprador](/lexico/#l7-usuario) deve ser capaz de personalizar a lista de [anúncios](/lexico/#l1-anuncio) exibidos para listarem apenas os que possuam tópicos de seu interesse | **Could** | [IF-28](/requisitos/introspeccao/#requisitos), [BF-22](/requisitos/brainstorming/#funcionais) |
| RF-29 | O [usuário](/lexico/#l7-usuario) deve ser capaz de alterar seus dados (email, nome, telefone, senha, endereço, foto de perfil) | **Must** |[BF-4](/requisitos/brainstorming/#funcionais) |
| RF-30 | O [usuário](/lexico/#l7-usuario) deve ser capaz de desativar sua conta | **Should** |[BF-5](/requisitos/brainstorming/#funcionais) |
| RF-31 | O [usuário](/lexico/#l7-usuario) deve ser capaz de excluir sua conta | **Must** |[BF-6](/requisitos/brainstorming/#funcionais) |
| RF-32 | O [usuário](/lexico/#l7-usuario) deve ser capaz de realizar login utilizando impressão digital | **Won't** |[BF-7](/requisitos/brainstorming/#funcionais) |
| RF-33 | O [comprador](/lexico/#l7-usuario), [vendedor](/lexico/#l7-usuario) e [moderador](/lexico/#l7-usuario) deve ser capaz de acessar o perfil de outros [compradores](/lexico/#l7-usuario) e [vendedores](/lexico/#l7-usuario) | **Should** | [BF-19](/requisitos/brainstorming/#funcionais), [QF-5](/requisitos/questionario/#funcionais) |
| RF-34 | O [moderador](/lexico/#l7-usuario) deve ser capaz de excluir um [anúncio](/lexico/#l1-anuncio) | **Could** | [BF-16](/requisitos/brainstorming/#funcionais) |
| RF-35 | O [comprador](/lexico/#l7-usuario) e [vendedor](/lexico/#l7-usuario) deve ser capaz de bloquear mensagens de outros [compradores](/lexico/#l7-usuario) e [vendedores](/lexico/#l7-usuario) | **Could** | [BF-20](/requisitos/brainstorming/#funcionais) |
| RF-36 | O [usuário](/lexico/#l7-usuario) deve ser capaz de interagir (visualizar e acessar) com o feed de [anúncios](/lexico/#l1-anuncio) | **Must** | [BF-21](/requisitos/brainstorming/#funcionais), [QF-6](/requisitos/questionario/#funcionais) |
| RF-37 | O sistema deve utilizar reconhecimento de imagem nas fotos dos jogos para aferir a qualidade da mídia | **Won't** | [BF-23](/requisitos/brainstorming/#funcionais) |
| RF-38 | O sistema deve utilizar reconhecimento de imagem nas fotos de usuário e anúncios para filtrar imagens impróprias | **Won't** | [BF-24](/requisitos/brainstorming/#funcionais) |
| RF-39 | O [vendedor](/lexico/#l7-usuario) deve ser capaz de adicionar palavras chave a um [anúncio](/lexico/#l1-anuncio) | **Could** | [BF-13](/requisitos/brainstorming/#funcionais) |
| RF-40 | O [usuário](/lexico/#l7-usuario) deve ser capaz de acessar uma página de ajuda e suporte | **Could** | [QF-3](/requisitos/questionario/#funcionais) |
| RF-41 | O [usuário](/lexico/#l7-usuario) deve ser capaz de visualizar a média das [avaliações](/lexico/#l5-avaliar) de [compradores](/lexico/#l7-usuario) e [vendedores](/lexico/#l7-usuario) | **Must** | [QF-11](/requisitos/questionario/#funcionais) |

### Não Funcionais

| Identificador | Requisito | Prioridade | Rastreabilidade |
|:--:|--|:--:|:--:|
| RNF-01 | O sistema deve informar o comprador e vendedor que as mensagens poderão ser verificadas em caso de denúncias | **Must** | [INF-29](/requisitos/introspeccao/#requisitos) |
| RNF-02 | O sistema deve possibilitar uma navegabilidade ágil entre as funcionalidades [**(a ser decidido)**](/requisitos/padroes/#a-ser-decidido) | **Should** | [INF-30](/requisitos/introspeccao/#requisitos) |
| RNF-03 | A interface do sistema deverá possuir uma boa usabilidade e de fácil aprendizado [**(a ser decidido)**](/requisitos/padroes/#a-ser-decidido) | **Should** | [INF-31](/requisitos/introspeccao/#requisitos), [BNF-6](/requisitos/brainstorming/#nao-funcionais), [QNF-4](/requisitos/questionario/#nao-funcionais) |
| RNF-04 | O sistema de mensagens deve buscar novas mensagens em no máximo 5 segundos | **Must** | [INF-32](/requisitos/introspeccao/#requisitos) |
| RNF-05 | O sistema deve funcionar em *smartphones* | **Must** | [INF-33](/requisitos/introspeccao/#requisitos) |
| RNF-06 | O sistema deve enviar um e-mail de confirmação para o [usuário](/lexico/#l7-usuario) após o cadastro | **Should** | [BNF-1](/requisitos/brainstorming/#nao-funcionais) |
| RNF-07 | O sistema deve fornecer um modo noturno | **Could** | [BNF-2](/requisitos/brainstorming/#nao-funcionais) |
| RNF-08 | O sistema deve possuir uma página de criação de anúncios intuitiva [**(a ser decidido)**](/requisitos/padroes/#a-ser-decidido) | **Should** | [BNF-3](/requisitos/brainstorming/#nao-funcionais) |
| RNF-09 | O sistema deve ser gamificado [**(a ser decidido)**](/requisitos/padroes/#a-ser-decidido) | **Could** | [BNF-4](/requisitos/brainstorming/#nao-funcionais) |
| RNF-10 | O sistema deve ser amigável [**(a ser decidido)**](/requisitos/padroes/#a-ser-decidido) | **Should** | [BNF-5](/requisitos/brainstorming/#nao-funcionais) |
| RNF-11 | O sistema deve exibir somente perfis de [compradores](/lexico/#l7-usuario) e [vendedores](/lexico/#l7-usuario) | **Should** | [BNF-7](/requisitos/brainstorming/#nao-funcionais) |
| RNF-12 | O sistema deve filtrar palavras impróprias em [anúncios](/lexico/#l1-anuncio) [**(a ser decidido)**](/requisitos/padroes/#a-ser-decidido) | **Could** | [BNF-8](/requisitos/brainstorming/#nao-funcionais) |
| RNF-13 | O sistema deve manter a senha do [usuário](/lexico/#l7-usuario) encriptada | **Must** | [QNF-1](/requisitos/questionario/#nao-funcionais) |
| RNF-14 | O sistema deve ser capaz de responder as requisições do [usuário](/lexico/#l7-usuario) rapidamente [**(a ser decidido)**](/requisitos/padroes/#a-ser-decidido) | **Must** | [QNF-2](/requisitos/questionario/#nao-funcionais) |
| RNF-15 | O sistema deve ser confiável [**(a ser decidido)**](/requisitos/padroes/#a-ser-decidido) | **Must** | [QNF-3](/requisitos/questionario/#nao-funcionais) |
| RNF-16 | O sistema deve dispor os [anúncios](/lexico/#l1-anuncio) de maneira organizada [**(a ser decidido)**](/requisitos/padroes/#a-ser-decidido) | **Should** | [QNF-5](/requisitos/questionario/#nao-funcionais) |

## Referências

> WIEGERS, Karl; BEATTY, Joy. "Software Requirements". Microsoft Press, 2013.

## Versionamento

| Versão | Data       | Modificação                    | Motivo | Autor         |
| ------ | ---------- | -------------------------------| ------ | ------------- |
| 1.0 | 17/02/2021 | Criação do documento | Listar, identificar e priorizar todos os requisitos e suas respectivas técnicas | Todos os integrantes |
