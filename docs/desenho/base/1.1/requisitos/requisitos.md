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
    - Refere-se ao número do requisito no [Documento de Brainstorming](/desenho/base/1.1/requisitos/brainstorming/)
    - Tipo: F para requisitos funcionais, NF para requisitos não funcionais
    - Exemplo: BF-4 Refere-se ao requisito funcional de número 4. BNF-2 Refere-se ao requisito não funcional de número 2.
- ITipo-número
    - Refere-se ao número do requisito no [Documento de Introspecção](/desenho/base/1.1/requisitos/introspeccao/)
    - Tipo: F para requisitos funcionais, NF para requisitos não funcionais
    - Exemplo: IF-1 Refere-se ao requisito funcional de número 1 do [Documento de Introspecção](/desenho/base/1.1/requisitos/introspeccao/), INF-1 Refere-se ao requisito não funcional de número 1 do [documento de Introspecção](/desenho/base/1.1/requisitos/introspeccao/)
- QTipo-número
    - Refere-se ao número do requisito no [Documento de Questionário](/desenho/base/1.1/requisitos/questionario/)
    - Tipo: F para requisitos funcionais, NF para requisitos não funcionais
    - Exemplo: QF-4 Refere-se ao requisito funcional de número 4 do documento de [Questionário](/desenho/base/1.1/requisitos/questionario/). QNF-2 Refere-se ao requisito não funcional de número 2 do [Documento de Questionário](/desenho/base/1.1/requisitos/questionario/).

### Funcionais

| Identificador | Requisito | Prioridade | Rastreabilidade |
|:--:|--|:--:|:--:|
| RF-01 | O [vendedor](/desenho/base/1.1/lexico/#l7-usuario) e [comprador](/desenho/base/1.1/lexico/#l7-usuario) devem ser capazes de se cadastrarem usando sua conta do Google | **Should** | [IF-1](/desenho/base/1.1/requisitos/introspeccao/#requisitos), [BF-3](/desenho/base/1.1/requisitos/brainstorming/#requisitos), [QF-10](/desenho/base/1.1/requisitos/questionario/#funcionais) |
| RF-02 | O [vendedor](/desenho/base/1.1/lexico/#l7-usuario) e [comprador](/desenho/base/1.1/lexico/#l7-usuario) devem ser capazes de se cadastrarem usando sua conta do Facebook | **Should** |[IF-2](/desenho/base/1.1/requisitos/introspeccao/#requisitos), [BF-2](/desenho/base/1.1/requisitos/brainstorming/#requisitos), [QF-9](/desenho/base/1.1/requisitos/questionario/#funcionais) |
| RF-03 | O [vendedor](/desenho/base/1.1/lexico/#l7-usuario) e [comprador](/desenho/base/1.1/lexico/#l7-usuario) devem ser capazes de criarem uma conta do sistema utilizando seu e-mail | **Must** | [IF-3](/desenho/base/1.1/requisitos/introspeccao/#requisitos), [BF-1](/desenho/base/1.1/requisitos/brainstorming/#funcionais), [QF-8](/desenho/base/1.1/requisitos/questionario/#funcionais) |
| RF-04 | O [comprador](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de [reportar](/desenho/base/1.1/lexico/#l6-reportar) um [anúncio](/desenho/base/1.1/lexico/#l) feito por um  [vendedor](/desenho/base/1.1/lexico/#l7-usuario)|  **Must**|  [IF-4](/desenho/base/1.1/requisitos/introspeccao/#requisitos)  
| RF-05 | O [comprador](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de [avaliar](/desenho/base/1.1/lexico/#l5-avaliar) um [vendedor](/desenho/base/1.1/lexico/#l7-usuario) após realizar uma [troca](/desenho/base/1.1/lexico/#l3-trocar) ou [venda](/desenho/base/1.1/lexico/#l2-vender) | **Must** | [IF-5](/desenho/base/1.1/requisitos/introspeccao/#requisitos), [BF-8](/desenho/base/1.1/requisitos/brainstorming/#funcionais), [QF-4](/desenho/base/1.1/requisitos/questionario/#funcionais) |
| RF-06 | O [vendedor](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de [avaliar](/desenho/base/1.1/lexico/#l5-avaliar) um [comprador](/desenho/base/1.1/lexico/#l7-usuario) após a realização de uma [venda](/desenho/base/1.1/lexico/#l2-vender) ou [troca](/desenho/base/1.1/lexico/#l3-trocar) | **Must** | [IF-6](/desenho/base/1.1/requisitos/introspeccao/#requisitos), [BF-9](/desenho/base/1.1/requisitos/brainstorming/#funcionais), [QF-4](/desenho/base/1.1/requisitos/questionario/#funcionais) |
| RF-07 | O [comprador](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de visualizar as informações dos [anúncios](/desenho/base/1.1/lexico/#l1-anuncio) | **Must** | [IF-7](/desenho/base/1.1/requisitos/introspeccao/#requisitos), [BF-17](/desenho/base/1.1/requisitos/brainstorming/#requisitos), [QF-1](/desenho/base/1.1/requisitos/questionario/#funcionais), [QF-12](/desenho/base/1.1/requisitos/questionario/#funcionais) |
| RF-08 | O [vendedor](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de cadastrar um novo [anúncio](/desenho/base/1.1/lexico/#l1-anuncio) | **Must** | [IF-8](/desenho/base/1.1/requisitos/introspeccao/#requisitos), [BF-11](/desenho/base/1.1/requisitos/brainstorming/#funcionais) |
| RF-09 | O [comprador](/desenho/base/1.1/lexico/#l7-usuario), após ter interagido com [vendedor](/desenho/base/1.1/lexico/#l7-usuario), deve ser capaz de [reportar](/desenho/base/1.1/lexico/#l6-reportar) o [vendedor](/desenho/base/1.1/lexico/#l7-usuario) | **Must** | [IF-9](/desenho/base/1.1/requisitos/introspeccao/#requisitos), [BF-10](/desenho/base/1.1/requisitos/brainstorming/#requisitos) |
| RF-10 | O [vendedor](/desenho/base/1.1/lexico/#l7-usuario), após ter interagido com [comprador](/desenho/base/1.1/lexico/#l7-usuario), deve ser capaz de [reportar](/desenho/base/1.1/lexico/#l6-reportar) o [comprador](/desenho/base/1.1/lexico/#l7-usuario) | **Must** | [IF-10](/desenho/base/1.1/requisitos/introspeccao/#requisitos) |
| RF-11 | O sistema deve fornecer um sistema de mensagens para o [comprador](/desenho/base/1.1/lexico/#l7-usuario) e o [vendedor](/desenho/base/1.1/lexico/#l7-usuario) interagirem | **Should** | [IF-11](/desenho/base/1.1/requisitos/introspeccao/#requisitos), [BF-14](/desenho/base/1.1/requisitos/brainstorming/#requisitos), [QF-2](/desenho/base/1.1/requisitos/questionario/#funcionais) |
| RF-12 | O sistema deve salvar um [anúncio](/desenho/base/1.1/lexico/#l1-anuncio) com as seguintes características: nome do(s) [jogo(s)](/desenho/base/1.1/lexico/#l4-jogo), plataforma, condição, foto(s), informações do [vendedor](/desenho/base/1.1/lexico/#l7-usuario), localização, preço e descrição | **Must** | [IF-12](/desenho/base/1.1/requisitos/introspeccao/#requisitos), [BF-12](/desenho/base/1.1/requisitos/brainstorming/#funcionais) |
| RF-13 | O sistema deve persistir as mensagens entre o [comprador](/desenho/base/1.1/lexico/#l7-usuario) e [vendedor](/desenho/base/1.1/lexico/#l7-usuario) de um determinado [anúncio](/desenho/base/1.1/lexico/#l1-anuncio) por 7 dias após o fechamento desse [anúncio](/desenho/base/1.1/lexico/#l1-anuncio), contanto que não haja nenhuma denúncia do [comprador](/desenho/base/1.1/lexico/#l7-usuario) ou [vendedor](/desenho/base/1.1/lexico/#l7-usuario). Nesse caso, as mensagens deverão ser mantidas até a resolução da denúncia. | **Should** | [IF-13](/desenho/base/1.1/requisitos/introspeccao/#requisitos) |
| RF-14 | O sistema deve manter as mensagens entre o [comprador](/desenho/base/1.1/lexico/#l7-usuario) e [vendedor](/desenho/base/1.1/lexico/#l7-usuario) disponíveis para que elas possam ser avaliadas, por moderadores, no caso de denúncias | **Should** | [IF-14](/desenho/base/1.1/requisitos/introspeccao/#requisitos) |
| RF-15 | O moderador deve ser capaz de [invalidar](/desenho/base/1.1/lexico/#l8-invalidar) um [anúncio](/desenho/base/1.1/lexico/#l1-anuncio) | **Could** | [IF-15](/desenho/base/1.1/requisitos/introspeccao/#requisitos) |
| RF-16 | O sistema deverá notificar o [vendedor](/desenho/base/1.1/lexico/#l7-usuario) caso seu [anúncio](/desenho/base/1.1/lexico/#l1-anuncio) seja [invalidado](/desenho/base/1.1/lexico/#l8-invalidar) | **Could** | [IF-16](/desenho/base/1.1/requisitos/introspeccao/#requisitos) |
| RF-17 | O sistema deve listar apenas [anúncios válidos](/desenho/base/1.1/lexico/#l9-anuncio-valido) | **Could** | [IF-17](/desenho/base/1.1/requisitos/introspeccao/#requisitos) |
| RF-18 | O sistema deverá notificar o [usuário](/desenho/base/1.1/lexico/#l7-usuario) quando um [anúncio](/desenho/base/1.1/lexico/#l1-anuncio) que ele reportou for [invalidado](/desenho/base/1.1/lexico/#l8-invalidar) | **Could** | [IF-18](/desenho/base/1.1/requisitos/introspeccao/#requisitos) |
| RF-19 | O [vendedor](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de remover um [anúncio](/desenho/base/1.1/lexico/#l1-anuncio) | **Must** | [IF-19](/desenho/base/1.1/requisitos/introspeccao/#requisitos) |
| RF-20 | O [vendedor](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de editar um anúncio | **Must** | [IF-20](/desenho/base/1.1/requisitos/introspeccao/#requisitos) |
| RF-21 | O sistema deve notificar o [comprador](/desenho/base/1.1/lexico/#l7-usuario) e [vendedor](/desenho/base/1.1/lexico/#l7-usuario) de novas mensagens | **Should** | [IF-21](/desenho/base/1.1/requisitos/introspeccao/#requisitos) |
| RF-22 | O [moderador](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de visualizar as denúncias de [anúncios](/desenho/base/1.1/lexico/#l1-anuncio), [vendedores](/desenho/base/1.1/lexico/#l7-usuario) e [compradores](/desenho/base/1.1/lexico/#l7-usuario) | **Could** | [IF-22](/desenho/base/1.1/requisitos/introspeccao/#requisitos) |
| RF-23 | O [moderador](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de banir um [usuário](/desenho/base/1.1/lexico/#l7-usuario) [**(a ser decidido)**](/desenho/base/1.1/requisitos/padroes/#a-ser-decidido) | **Could** | [IF-23](/desenho/base/1.1/requisitos/introspeccao/#requisitos), [BF-15](/desenho/base/1.1/requisitos/brainstorming/#requisitos) |
| RF-24 | O sistema no momento de cadastro, deve pedir o consentimento dos [usuários](/desenho/base/1.1/lexico/#l7-usuario) em relação aos termos de uso [**(a ser decidido)**](/desenho/base/1.1/requisitos/padroes/#a-ser-decidido) | **Must** | [IF-24](/desenho/base/1.1/requisitos/introspeccao/#requisitos) |
| RF-25 | O sistema deve salvar [usuários](/desenho/base/1.1/lexico/#l7-usuario) com as seguintes características: nome, apelido (nome de [usuário](/desenho/base/1.1/lexico/#l7-usuario)), email e senha | **Must** | [IF-25](/desenho/base/1.1/requisitos/introspeccao/#requisitos) |
| RF-26 | O [comprador](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de visualizar todos os [anúncios válidos](/desenho/base/1.1/lexico/#l9-anuncio-valido) cadastrados | **Could** | [IF-26](/desenho/base/1.1/requisitos/introspeccao/#requisitos) |
| RF-27 | O [comprador](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de filtrar os [anúncios](/desenho/base/1.1/lexico/#l1-anuncio) por suas informações | **Should** | [IF-27](/desenho/base/1.1/requisitos/introspeccao/#requisitos), [BF-18](/desenho/base/1.1/requisitos/brainstorming/#funcionais), [QF-7](/desenho/base/1.1/requisitos/questionario/#funcionais) |
| RF-28 | O [comprador](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de personalizar a lista de [anúncios](/desenho/base/1.1/lexico/#l1-anuncio) exibidos para listarem apenas os que possuam tópicos de seu interesse | **Could** | [IF-28](/desenho/base/1.1/requisitos/introspeccao/#requisitos), [BF-22](/desenho/base/1.1/requisitos/brainstorming/#funcionais) |
| RF-29 | O [usuário](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de alterar seus dados (email, nome, telefone, senha, endereço, foto de perfil) | **Must** |[BF-4](/desenho/base/1.1/requisitos/brainstorming/#funcionais) |
| RF-30 | O [usuário](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de desativar sua conta | **Should** |[BF-5](/desenho/base/1.1/requisitos/brainstorming/#funcionais) |
| RF-31 | O [usuário](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de excluir sua conta | **Must** |[BF-6](/desenho/base/1.1/requisitos/brainstorming/#funcionais) |
| RF-32 | O [usuário](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de realizar login utilizando impressão digital | **Won't** |[BF-7](/desenho/base/1.1/requisitos/brainstorming/#funcionais) |
| RF-33 | O [comprador](/desenho/base/1.1/lexico/#l7-usuario), [vendedor](/desenho/base/1.1/lexico/#l7-usuario) e [moderador](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de acessar o perfil de outros [compradores](/desenho/base/1.1/lexico/#l7-usuario) e [vendedores](/desenho/base/1.1/lexico/#l7-usuario) | **Should** | [BF-19](/desenho/base/1.1/requisitos/brainstorming/#funcionais), [QF-5](/desenho/base/1.1/requisitos/questionario/#funcionais) |
| RF-34 | O [moderador](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de excluir um [anúncio](/desenho/base/1.1/lexico/#l1-anuncio) | **Could** | [BF-16](/desenho/base/1.1/requisitos/brainstorming/#funcionais) |
| RF-35 | O [comprador](/desenho/base/1.1/lexico/#l7-usuario) e [vendedor](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de bloquear mensagens de outros [compradores](/desenho/base/1.1/lexico/#l7-usuario) e [vendedores](/desenho/base/1.1/lexico/#l7-usuario) | **Could** | [BF-20](/desenho/base/1.1/requisitos/brainstorming/#funcionais) |
| RF-36 | O [usuário](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de interagir com o feed de [anúncios](/desenho/base/1.1/lexico/#l1-anuncio) acessando os [anúncios](/desenho/base/1.1/lexico/#l1-anuncio) a partir dele | **Must** | [BF-21](/desenho/base/1.1/requisitos/brainstorming/#funcionais), [QF-6](/desenho/base/1.1/requisitos/questionario/#funcionais) |
| RF-37 | O sistema deve utilizar reconhecimento de imagem nas fotos dos jogos para aferir a qualidade da mídia | **Won't** | [BF-23](/desenho/base/1.1/requisitos/brainstorming/#funcionais) |
| RF-38 | O sistema deve utilizar reconhecimento de imagem nas fotos de usuário e anúncios para filtrar imagens impróprias | **Won't** | [BF-24](/desenho/base/1.1/requisitos/brainstorming/#funcionais) |
| RF-39 | O [vendedor](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de adicionar palavras chave a um [anúncio](/desenho/base/1.1/lexico/#l1-anuncio) | **Could** | [BF-13](/desenho/base/1.1/requisitos/brainstorming/#funcionais) |
| RF-40 | O [usuário](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de acessar uma página de ajuda e suporte | **Could** | [QF-3](/desenho/base/1.1/requisitos/questionario/#funcionais) |
| RF-41 | O [usuário](/desenho/base/1.1/lexico/#l7-usuario) deve ser capaz de visualizar a média das [avaliações](/desenho/base/1.1/lexico/#l5-avaliar) de [compradores](/desenho/base/1.1/lexico/#l7-usuario) e [vendedores](/desenho/base/1.1/lexico/#l7-usuario) | **Must** | [QF-11](/desenho/base/1.1/requisitos/questionario/#funcionais) |

### Não Funcionais

| Identificador | Requisito | Prioridade | Rastreabilidade |
|:--:|--|:--:|:--:|
| RNF-01 | O sistema deve informar o comprador e vendedor que as mensagens poderão ser verificadas em caso de denúncias | **Must** | [INF-29](/desenho/base/1.1/requisitos/introspeccao/#requisitos) |
| RNF-02 | O sistema deve possibilitar uma navegabilidade ágil entre as funcionalidades [**(a ser decidido)**](/desenho/base/1.1/requisitos/padroes/#a-ser-decidido) | **Should** | [INF-30](/desenho/base/1.1/requisitos/introspeccao/#requisitos) |
| RNF-03 | A interface do sistema deverá possuir uma boa usabilidade e de fácil aprendizado [**(a ser decidido)**](/desenho/base/1.1/requisitos/padroes/#a-ser-decidido) | **Should** | [INF-31](/desenho/base/1.1/requisitos/introspeccao/#requisitos), [BNF-6](/desenho/base/1.1/requisitos/brainstorming/#nao-funcionais), [QNF-4](/desenho/base/1.1/requisitos/questionario/#nao-funcionais) |
| RNF-04 | O sistema de mensagens deve buscar novas mensagens em no máximo 5 segundos | **Must** | [INF-32](/desenho/base/1.1/requisitos/introspeccao/#requisitos) |
| RNF-05 | O sistema deve funcionar em *smartphones* | **Must** | [INF-33](/desenho/base/1.1/requisitos/introspeccao/#requisitos) |
| RNF-06 | O sistema deve enviar um e-mail de confirmação para o [usuário](/desenho/base/1.1/lexico/#l7-usuario) após o cadastro | **Should** | [BNF-1](/desenho/base/1.1/requisitos/brainstorming/#nao-funcionais) |
| RNF-07 | O sistema deve fornecer um modo noturno | **Could** | [BNF-2](/desenho/base/1.1/requisitos/brainstorming/#nao-funcionais) |
| RNF-08 | O sistema deve possuir uma página de criação de anúncios intuitiva [**(a ser decidido)**](/desenho/base/1.1/requisitos/padroes/#a-ser-decidido) | **Should** | [BNF-3](/desenho/base/1.1/requisitos/brainstorming/#nao-funcionais) |
| RNF-09 | O sistema deve ser gamificado [**(a ser decidido)**](/desenho/base/1.1/requisitos/padroes/#a-ser-decidido) | **Could** | [BNF-4](/desenho/base/1.1/requisitos/brainstorming/#nao-funcionais) |
| RNF-10 | O sistema deve ser amigável [**(a ser decidido)**](/desenho/base/1.1/requisitos/padroes/#a-ser-decidido) | **Should** | [BNF-5](/desenho/base/1.1/requisitos/brainstorming/#nao-funcionais) |
| RNF-11 | O sistema deve exibir somente perfis de [compradores](/desenho/base/1.1/lexico/#l7-usuario) e [vendedores](/desenho/base/1.1/lexico/#l7-usuario) | **Should** | [BNF-7](/desenho/base/1.1/requisitos/brainstorming/#nao-funcionais) |
| RNF-12 | O sistema deve filtrar palavras impróprias em [anúncios](/desenho/base/1.1/lexico/#l1-anuncio) [**(a ser decidido)**](/desenho/base/1.1/requisitos/padroes/#a-ser-decidido) | **Could** | [BNF-8](/desenho/base/1.1/requisitos/brainstorming/#nao-funcionais) |
| RNF-13 | O sistema deve manter a senha do [usuário](/desenho/base/1.1/lexico/#l7-usuario) encriptada | **Must** | [QNF-1](/desenho/base/1.1/requisitos/questionario/#nao-funcionais) |
| RNF-14 | O sistema deve ser capaz de responder as requisições do [usuário](/desenho/base/1.1/lexico/#l7-usuario) rapidamente [**(a ser decidido)**](/desenho/base/1.1/requisitos/padroes/#a-ser-decidido) | **Must** | [QNF-2](/desenho/base/1.1/requisitos/questionario/#nao-funcionais) |
| RNF-15 | O sistema deve ser confiável [**(a ser decidido)**](/desenho/base/1.1/requisitos/padroes/#a-ser-decidido) | **Must** | [QNF-3](/desenho/base/1.1/requisitos/questionario/#nao-funcionais) |
| RNF-16 | O sistema deve dispor os [anúncios](/desenho/base/1.1/lexico/#l1-anuncio) de maneira organizada [**(a ser decidido)**](/desenho/base/1.1/requisitos/padroes/#a-ser-decidido) | **Should** | [QNF-5](/desenho/base/1.1/requisitos/questionario/#nao-funcionais) |

## Referências

> WIEGERS, Karl; BEATTY, Joy. "Software Requirements". Microsoft Press, 2013.

## Versionamento

| Versão | Data       | Modificação                    | Motivo | Autor         |
| ------ | ---------- | -------------------------------| ------ | ------------- |
| [1.0](../../../../versoes/requisitos/1.0.md) | 17/02/2021 | Criação do documento | Listar, identificar e priorizar todos os requisitos e suas respectivas técnicas | Todos os integrantes |
| 2.0 | 17/02/2021 | Modificando os "e" para "," na coluna de rastreabilidade e corrigindo incoerências no RF-36 | Correção para seguir o padrão e corrigindo incoerências | Washington Bispo |
