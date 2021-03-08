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
    - Refere-se ao número do requisito no [Documento de Brainstorming](../brainstorming/)
    - Tipo: F para requisitos funcionais, NF para requisitos não funcionais
    - Exemplo: BF-4 Refere-se ao requisito funcional de número 4. BNF-2 Refere-se ao requisito não funcional de número 2.
- ITipo-número
    - Refere-se ao número do requisito no [Documento de Introspecção](../introspeccao/)
    - Tipo: F para requisitos funcionais, NF para requisitos não funcionais
    - Exemplo: IF-1 Refere-se ao requisito funcional de número 1 do [Documento de Introspecção](../introspeccao/), INF-1 Refere-se ao requisito não funcional de número 1 do [documento de Introspecção](../introspeccao/)
- QTipo-número
    - Refere-se ao número do requisito no [Documento de Questionário](../questionario/)
    - Tipo: F para requisitos funcionais, NF para requisitos não funcionais
    - Exemplo: QF-4 Refere-se ao requisito funcional de número 4 do documento de [Questionário](../questionario/). QNF-2 Refere-se ao requisito não funcional de número 2 do [Documento de Questionário](../questionario/).

### Funcionais

| Identificador | Requisito | Prioridade | Rastreabilidade |
|:--:|--|:--:|:--:|
| RF-01 | O [vendedor](../../lexico/#l7-usuario) e [comprador](../../lexico/#l7-usuario) devem ser capazes de se cadastrarem usando sua conta do Google | **Should** | [IF-1](../introspeccao/#requisitos), [BF-3](../brainstorming/#requisitos), [QF-10](../questionario/#funcionais) |
| RF-02 | O [vendedor](../../lexico/#l7-usuario) e [comprador](../../lexico/#l7-usuario) devem ser capazes de se cadastrarem usando sua conta do Facebook | **Should** |[IF-2](../introspeccao/#requisitos), [BF-2](../brainstorming/#requisitos), [QF-9](../questionario/#funcionais) |
| RF-03 | O [vendedor](../../lexico/#l7-usuario) e [comprador](../../lexico/#l7-usuario) devem ser capazes de criarem uma conta do sistema utilizando seu e-mail | **Must** | [IF-3](../introspeccao/#requisitos), [BF-1](../brainstorming/#funcionais), [QF-8](../questionario/#funcionais) |
| RF-04 | O [comprador](../../lexico/#l7-usuario) deve ser capaz de [reportar](../../lexico/#l6-reportar) um [anúncio](../../lexico/#l) feito por um  [vendedor](../../lexico/#l7-usuario)|  **Must**|  [IF-4](../introspeccao/#requisitos)  
| RF-05 | O [comprador](../../lexico/#l7-usuario) deve ser capaz de [avaliar](../../lexico/#l5-avaliar) um [vendedor](../../lexico/#l7-usuario) após realizar uma [troca](../../lexico/#l3-trocar) ou [venda](../../lexico/#l2-vender) | **Must** | [IF-5](../introspeccao/#requisitos), [BF-8](../brainstorming/#funcionais), [QF-4](../questionario/#funcionais) |
| RF-06 | O [vendedor](../../lexico/#l7-usuario) deve ser capaz de [avaliar](../../lexico/#l5-avaliar) um [comprador](../../lexico/#l7-usuario) após a realização de uma [venda](../../lexico/#l2-vender) ou [troca](../../lexico/#l3-trocar) | **Must** | [IF-6](../introspeccao/#requisitos), [BF-9](../brainstorming/#funcionais), [QF-4](../questionario/#funcionais) |
| RF-07 | O [comprador](../../lexico/#l7-usuario) deve ser capaz de visualizar as informações dos [anúncios](../../lexico/#l1-anuncio) | **Must** | [IF-7](../introspeccao/#requisitos), [BF-17](../brainstorming/#requisitos), [QF-1](../questionario/#funcionais), [QF-12](../questionario/#funcionais) |
| RF-08 | O [vendedor](../../lexico/#l7-usuario) deve ser capaz de cadastrar um novo [anúncio](../../lexico/#l1-anuncio) | **Must** | [IF-8](../introspeccao/#requisitos), [BF-11](../brainstorming/#funcionais) |
| RF-09 | O [comprador](../../lexico/#l7-usuario), após ter interagido com [vendedor](../../lexico/#l7-usuario), deve ser capaz de [reportar](../../lexico/#l6-reportar) o [vendedor](../../lexico/#l7-usuario) | **Must** | [IF-9](../introspeccao/#requisitos), [BF-10](../brainstorming/#requisitos) |
| RF-10 | O [vendedor](../../lexico/#l7-usuario), após ter interagido com [comprador](../../lexico/#l7-usuario), deve ser capaz de [reportar](../../lexico/#l6-reportar) o [comprador](../../lexico/#l7-usuario) | **Must** | [IF-10](../introspeccao/#requisitos) |
| RF-11 | O sistema deve fornecer um sistema de mensagens para o [comprador](../../lexico/#l7-usuario) e o [vendedor](../../lexico/#l7-usuario) interagirem | **Should** | [IF-11](../introspeccao/#requisitos), [BF-14](../brainstorming/#requisitos), [QF-2](../questionario/#funcionais) |
| RF-12 | O sistema deve salvar um [anúncio](../../lexico/#l1-anuncio) com as seguintes características: nome do(s) [jogo(s)](../../lexico/#l4-jogo), plataforma, condição, foto(s), informações do [vendedor](../../lexico/#l7-usuario), localização, preço e descrição | **Must** | [IF-12](../introspeccao/#requisitos), [BF-12](../brainstorming/#funcionais) |
| RF-13 | O sistema deve persistir as mensagens entre o [comprador](../../lexico/#l7-usuario) e [vendedor](../../lexico/#l7-usuario) de um determinado [anúncio](../../lexico/#l1-anuncio) por 7 dias após o fechamento desse [anúncio](../../lexico/#l1-anuncio), contanto que não haja nenhuma denúncia do [comprador](../../lexico/#l7-usuario) ou [vendedor](../../lexico/#l7-usuario). Nesse caso, as mensagens deverão ser mantidas até a resolução da denúncia. | **Should** | [IF-13](../introspeccao/#requisitos) |
| RF-14 | O sistema deve manter as mensagens entre o [comprador](../../lexico/#l7-usuario) e [vendedor](../../lexico/#l7-usuario) disponíveis para que elas possam ser avaliadas, por moderadores, no caso de denúncias | **Should** | [IF-14](../introspeccao/#requisitos) |
| RF-15 | O moderador deve ser capaz de [invalidar](../../lexico/#l8-invalidar) um [anúncio](../../lexico/#l1-anuncio) | **Could** | [IF-15](../introspeccao/#requisitos) |
| RF-16 | O sistema deverá notificar o [vendedor](../../lexico/#l7-usuario) caso seu [anúncio](../../lexico/#l1-anuncio) seja [invalidado](../../lexico/#l8-invalidar) | **Could** | [IF-16](../introspeccao/#requisitos) |
| RF-17 | O sistema deve listar apenas [anúncios válidos](../../lexico/#l9-anuncio-valido) | **Could** | [IF-17](../introspeccao/#requisitos) |
| RF-18 | O sistema deverá notificar o [usuário](../../lexico/#l7-usuario) quando um [anúncio](../../lexico/#l1-anuncio) que ele reportou for [invalidado](../../lexico/#l8-invalidar) | **Could** | [IF-18](../introspeccao/#requisitos) |
| RF-19 | O [vendedor](../../lexico/#l7-usuario) deve ser capaz de remover um [anúncio](../../lexico/#l1-anuncio) | **Must** | [IF-19](../introspeccao/#requisitos) |
| RF-20 | O [vendedor](../../lexico/#l7-usuario) deve ser capaz de editar um anúncio | **Must** | [IF-20](../introspeccao/#requisitos) |
| RF-21 | O sistema deve notificar o [comprador](../../lexico/#l7-usuario) e [vendedor](../../lexico/#l7-usuario) de novas mensagens | **Should** | [IF-21](../introspeccao/#requisitos) |
| RF-22 | O [moderador](../../lexico/#l7-usuario) deve ser capaz de visualizar as denúncias de [anúncios](../../lexico/#l1-anuncio), [vendedores](../../lexico/#l7-usuario) e [compradores](../../lexico/#l7-usuario) | **Could** | [IF-22](../introspeccao/#requisitos) |
| RF-23 | O [moderador](../../lexico/#l7-usuario) deve ser capaz de banir um [usuário](../../lexico/#l7-usuario) [**(a ser decidido)**](../padroes/#a-ser-decidido) | **Could** | [IF-23](../introspeccao/#requisitos), [BF-15](../brainstorming/#requisitos) |
| RF-24 | O sistema no momento de cadastro, deve pedir o consentimento dos [usuários](../../lexico/#l7-usuario) em relação aos termos de uso [**(a ser decidido)**](../padroes/#a-ser-decidido) | **Must** | [IF-24](../introspeccao/#requisitos) |
| RF-25 | O sistema deve salvar [usuários](../../lexico/#l7-usuario) com as seguintes características: nome, apelido (nome de [usuário](../../lexico/#l7-usuario)), email e senha | **Must** | [IF-25](../introspeccao/#requisitos) |
| RF-26 | O [comprador](../../lexico/#l7-usuario) deve ser capaz de visualizar todos os [anúncios válidos](../../lexico/#l9-anuncio-valido) cadastrados | **Could** | [IF-26](../introspeccao/#requisitos) |
| RF-27 | O [comprador](../../lexico/#l7-usuario) deve ser capaz de filtrar os [anúncios](../../lexico/#l1-anuncio) por suas informações | **Should** | [IF-27](../introspeccao/#requisitos), [BF-18](../brainstorming/#funcionais), [QF-7](../questionario/#funcionais) |
| RF-28 | O [comprador](../../lexico/#l7-usuario) deve ser capaz de personalizar a lista de [anúncios](../../lexico/#l1-anuncio) exibidos para listarem apenas os que possuam tópicos de seu interesse | **Could** | [IF-28](../introspeccao/#requisitos), [BF-22](../brainstorming/#funcionais) |
| RF-29 | O [usuário](../../lexico/#l7-usuario) deve ser capaz de alterar seus dados (email, nome, telefone, senha, endereço, foto de perfil) | **Must** |[BF-4](../brainstorming/#funcionais) |
| RF-30 | O [usuário](../../lexico/#l7-usuario) deve ser capaz de desativar sua conta | **Should** |[BF-5](../brainstorming/#funcionais) |
| RF-31 | O [usuário](../../lexico/#l7-usuario) deve ser capaz de excluir sua conta | **Must** |[BF-6](../brainstorming/#funcionais) |
| RF-32 | O [usuário](../../lexico/#l7-usuario) deve ser capaz de realizar login utilizando impressão digital | **Won't** |[BF-7](../brainstorming/#funcionais) |
| RF-33 | O [comprador](../../lexico/#l7-usuario), [vendedor](../../lexico/#l7-usuario) e [moderador](../../lexico/#l7-usuario) deve ser capaz de acessar o perfil de outros [compradores](../../lexico/#l7-usuario) e [vendedores](../../lexico/#l7-usuario) | **Should** | [BF-19](../brainstorming/#funcionais), [QF-5](../questionario/#funcionais) |
| RF-34 | O [moderador](../../lexico/#l7-usuario) deve ser capaz de excluir um [anúncio](../../lexico/#l1-anuncio) | **Could** | [BF-16](../brainstorming/#funcionais) |
| RF-35 | O [comprador](../../lexico/#l7-usuario) e [vendedor](../../lexico/#l7-usuario) deve ser capaz de bloquear mensagens de outros [compradores](../../lexico/#l7-usuario) e [vendedores](../../lexico/#l7-usuario) | **Could** | [BF-20](../brainstorming/#funcionais) |
| RF-36 | O [usuário](../../lexico/#l7-usuario) deve ser capaz de interagir com o feed de [anúncios](../../lexico/#l1-anuncio) acessando os [anúncios](../../lexico/#l1-anuncio) a partir dele | **Must** | [BF-21](../brainstorming/#funcionais), [QF-6](../questionario/#funcionais) |
| RF-37 | O sistema deve utilizar reconhecimento de imagem nas fotos dos jogos para aferir a qualidade da mídia | **Won't** | [BF-23](../brainstorming/#funcionais) |
| RF-38 | O sistema deve utilizar reconhecimento de imagem nas fotos de usuário e anúncios para filtrar imagens impróprias | **Won't** | [BF-24](../brainstorming/#funcionais) |
| RF-39 | O [vendedor](../../lexico/#l7-usuario) deve ser capaz de adicionar palavras chave a um [anúncio](../../lexico/#l1-anuncio) | **Could** | [BF-13](../brainstorming/#funcionais) |
| RF-40 | O [usuário](../../lexico/#l7-usuario) deve ser capaz de acessar uma página de ajuda e suporte | **Could** | [QF-3](../questionario/#funcionais) |
| RF-41 | O [usuário](../../lexico/#l7-usuario) deve ser capaz de visualizar a média das [avaliações](../../lexico/#l5-avaliar) de [compradores](../../lexico/#l7-usuario) e [vendedores](../../lexico/#l7-usuario) | **Must** | [QF-11](../questionario/#funcionais) |

### Não Funcionais

| Identificador | Requisito | Prioridade | Rastreabilidade |
|:--:|--|:--:|:--:|
| RNF-01 | O sistema deve informar o comprador e vendedor que as mensagens poderão ser verificadas em caso de denúncias | **Must** | [INF-29](../introspeccao/#requisitos) |
| RNF-04 | O sistema de mensagens deve buscar novas mensagens em no máximo 5 segundos | **Must** | [INF-32](../introspeccao/#requisitos) |
| RNF-05 | O sistema deve funcionar em *smartphones* seja Android ou iOS | **Must** | [INF-33](../introspeccao/#requisitos) |
| RNF-06 | O sistema deve enviar um e-mail de confirmação para o [usuário](../../lexico/#l7-usuario) após o cadastro | **Should** | [BNF-1](../brainstorming/#nao-funcionais) |
| RNF-07 | O sistema deve fornecer um modo noturno | **Could** | [BNF-2](../brainstorming/#nao-funcionais) |
| RNF-11 | O sistema deve exibir somente perfis de [compradores](../../lexico/#l7-usuario) e [vendedores](../../lexico/#l7-usuario) | **Should** | [BNF-7](../brainstorming/#nao-funcionais) |
| RNF-12 | O sistema deve filtrar palavras impróprias em [anúncios](../../lexico/#l1-anuncio) | **Could** | [BNF-8](../brainstorming/#nao-funcionais) |
| RNF-13 | O sistema deve manter a senha do [usuário](../../lexico/#l7-usuario) encriptada | **Must** | [QNF-1](../questionario/#nao-funcionais) |

### Qualidade

<p style="text-indent: 20px; text-align: justify">
Os requisitos de qualidade aqui listados foram obtidos realizando uma técnica de exploração dos atributos de qualidade do sistema e podem ser encontrados <a href="../../../../modelagem/iniciativa/atributos_qualidade">aqui</a>. Já o documento de especificação dos requisitos pode ser acessado <a href="../../../../modelagem/iniciativa/especificacao_suplementar">aqui</a>.
</p>

<p style="text-indent: 20px; text-align: justify">
As prioridades maiores representam requisitos que são mais relevantes. Mais detalhes sobre a priorização dos atributos de qualidade podem ser encontrados <a href="../../../../modelagem/iniciativa/atributos_qualidade/#passo-3-priorizar-a-lista">aqui</a>.
</p>

| Indentificador | Requisito | Prioridade | Atributo de qualidade |
|:--:|--|:--:|:--:|
| RNFQ-1 | O vendedor com experiência deve ser capaz de cadastrar um anúncio, desconsiderando o tempo para realizar as fotografias, em uma média de tempo de 8 minutos, com um máximo de 12 minutos, 90% das vezes | 3 | Usabilidade |
| RNFQ-2 | O sistema deve reutilizar os componentes já criados que se encaixem na tarefa necessária | 2 | Usabilidade, Reusabilidade |
| RNFQ-3 | O sistema deve utilizar um conjunto de ícones e *assets* padronizados, sempre com o mesmo propósito | 2 | Usabilidade, Reusabilidade |
| RNFQ-4 | O sistema deve informar erros em campos no formulário de cadastro de anúncio | 3 | Usabilidade |
| RNFQ-5 | O sistema deve informar erros com uma janela de tempo de no máximo 5 segundos | 3 | Usabilidade, Perfomance |
| RNFQ-6 | O sistema deve submeter requisições apenas se os campos forem válidos e estiverem corretos | 3 | Usabilidade, Perfomance |
| RNFQ-7 | O sistema deve permitir ao usuário cancelar a tarefa em execução antes da conclusão de pelo menos 50% da mesma | 3 | Usabilidade |
| RNFQ-8 | Antes de realizar uma requisição durante uma tarefa o sistema deve permitir ao usuário cancelar a tarefa | 3 | Usabilidade |
| RNFQ-9 | Os componentes do sistema devem resolver os problemas utilizando a menor quantidade de operações possível, no máximo 70% do processamento destinado a ele | 2 | Performance, Eficiência |
| RNFQ-10 | Os componentes do sistema devem resolver os problemas utilizando a menor quantidade de memória possível, no máximo 70% da memória destinado a ele | 2 | Performance, Eficiência |
| RNFQ-11 | O sistema deve solicitar um *CAPTCHA* sempre que o usuário errar a senha por 2 ou mais vezes consecutivas | 6 | Segurança |
| RNFQ-12 | O sistema deve solicitar a senha atual do usuário antes de desativar ou excluir a conta  | 6 |  Segurança |
| RNFQ-13 | O sistema deve solicitar confirmação do usuário por email antes de excluir a conta | 6 | Segurança |
| RNFQ-14 | O sistema deve ser eficaz em navegadores modernos, como Google Chrome, Mozilla Firefox, Microsoft Edge, Opera GX e Safari | 4 | Portabilidade |
| RNFQ-15 | O sistema deve carregar as páginas WEB em no máximo 10 segundos, dada uma rede de 10 ou mais megabits por segundo | 2 | Eficiência, Performance |
| RNFQ-16 | O sistema deve responder requisições em no máximo 5 segundos estritos | 2 | Eficiência, Performance |
| RNFQ-17 | O sistema deve recuperar os objetos do SGBD em no máximo 3 segundos | 2 | Eficiência, Performance |
| RNFQ-18 | O sistema não deve falhar em responder as requisições mais que 5 vezes em 1000 casos | 4 |Confiabilidade |
| RNFQ-19 | Os componentes do sistema não devem falhar mais do que uma vez entre 30 dias | 4 | Confiabilidade |
| RNFQ-20 | Os componentes do sistema devem se recuperar de uma falha simples em menos de 10s | 4 | Confiabilidade |

## Referências

> WIEGERS, Karl; BEATTY, Joy. "Software Requirements". Microsoft Press, 2013.

## Versionamento

| Versão | Data       | Modificação                    | Motivo | Autor         |
| ------ | ---------- | -------------------------------| ------ | ------------- |
| [1.0](../../../../../versoes/requisitos/1.0/) | 17/02/2021 | Criação do documento | Listar, identificar e priorizar todos os requisitos e suas respectivas técnicas | Todos os integrantes |
| [2.0](../../../../../versoes/requisitos/2.0/) | 17/02/2021 | Modificando os "e" para "," na coluna de rastreabilidade e corrigindo incoerências no RF-36 | Correção para seguir o padrão e corrigindo incoerências | Washington Bispo |
| 3.0 | 07/03/2021 | Inserindo requisitos não funcionais de qualidade e removendo os requisitos com a ser decidido | Para que os requisitos não funcionais estejam bem estruturados | Igor Paiva, Rhuan Queiroz, Thiago Guilherme, Thiago Lopes e Washingo Bispo |
