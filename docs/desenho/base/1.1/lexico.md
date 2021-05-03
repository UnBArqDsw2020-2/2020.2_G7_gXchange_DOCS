# Léxico

## Introdução

<p style="text-indent: 20px; text-align: justify">
Léxico trata-se de uma técnica que procura descrever os símbolos de uma linguagem, o
principal objetivo a ser perseguido pelos Engenheiros de Requisitos é a identificação de palavras ou
frases peculiares ao meio social da aplicação sob estudo. Cada símbolo é descrito com noção e
impacto.
</p>

## Metodologia

Utilizaremos como base o modelo de tabela abaixo:

### **Símbolo**

| Classificação       | Noção     | Impacto   | Sinônimos |
| ------------------- | --------- | --------- | :-------: |
| Objeto/Estado/Verbo | Denotação | Conotação | Opcional  |

## Léxicos

#### L1 - **Anúncio**

| Classificação | Noção                                                            | Impacto                                         | Sinônimos  |
| ------------- | ---------------------------------------------------------------- | ----------------------------------------------- | :-------: |
| Objeto        | Referente a publicação de um jogo disponível para troca ou venda | Usuário visualiza rapidamente diversos anúncios | Publicação |

#### L2 - **Vender**

| Classificação | Noção                              | Impacto                                                                   | Sinônimos |
| ------------- | ---------------------------------- | ------------------------------------------------------------------------- | :-------: |
| Verbo         | Forma de um usuário vender um jogo | O vendedor ao vender um de seus jogos permite ao comprador receber o jogo | -         |

#### L3 - **Trocar**

| Classificação | Noção                              | Impacto                                                                           | Sinônimos |
| ------------- | ---------------------------------- | --------------------------------------------------------------------------------- | :-------: |
| Verbo         | Forma de um usuário trocar um jogo | Dois usuários entram em acordo e trocam entre si as mídias físicas dos seus jogos | Escambo   |

#### L4 - **Jogo**

| Classificação | Noção                                                            | Impacto                                              | Sinônimos    |
| ------------- | ---------------------------------------------------------------- | ---------------------------------------------------- | :-------: |
| Objeto        | Um jogo digital em mídia física geralmente utilizado em consoles | Podem ser publicados para serem vendidos ou trocados | Mídia Física |

#### L5 - **Avaliar**

| Classificação | Noção                                              | Impacto                                                | Sinônimos |
| ------------- | -------------------------------------------------- | ------------------------------------------------------ | :-------: |
| Verbo         | Ato de um usuário ser avaliado por outros usuários | O usuário avaliado terá sua nota de avaliação alterada | -         |

#### L6 - **Reportar**

| Classificação | Noção                                                        | Impacto                                                                | Sinônimos |
| ------------- | ------------------------------------------------------------ | ---------------------------------------------------------------------- | :-------: |
| Verbo         | Ato de um usuário reportar uma publicação e/ou outro usuário | O usuário reportado ou publicação reportada será levado para avaliação | Denunciar |

#### L7 - **Usuário**

| Classificação | Noção | Impacto | Sinônimos |
| ------------- | ------| ------- | :-------: |
| Objeto | Qualquer pessoa que esteja utilizando o sistema, de acordo com o [perfil de usuário](../personas) definido | O usuário pode publicar, comprar, trocar [jogos](#l4-jogo) | Comprador, vendedor, moderador |

#### L8 - **Invalidar**

| Classificação | Noção  | Impacto | Sinônimos |
| ------------- | ------ | ------- | :-------: |
| Verbo | Ação do moderador de tornar um [anúncio inválido](#l10-anuncio-invalido) | Faz com que o anúncio se torne [inválido](#l10-anuncio-invalido) e não seja listado para os [usuários](#l7-usuario) | nulificar, anular |

#### L9 - **Anúncio válido**

| Classificação | Noção  | Impacto | Sinônimos |
| ------------- | ------ | ------- | :-------: |
| Estado | Um anúncio válido é listado para os [usuários](#l7-usuario) | Um anúncio é criado como válido e o moderador pode [invalidá-lo](#l8-invalidar) | - |

#### L10 - **Anúncio inválido**

| Classificação | Noção  | Impacto | Sinônimos |
| ------------- | ------ | ------- | :-------: |
| Estado | Um anúncio válido não é listado para os [usuários](#l7-usuario) | O moderador [invalida](#l8-invalidar) ou valida um anúncio | - |

#### L11 - **Conta**

| Classificação | Noção  | Impacto | Sinônimos |
| ------------- | ------ | ------- | :-------: |
| Objeto | Um conta representa o vínculo entre um usuário e o sistema gXchange, pode ser vinculada a uma conta google ou facebook e também, diretamente no sistema | Uma conta inicialmente está [ativa](#l12-conta-ativa) e pode ser [desativada](#l12-conta-desativada) pelo usuário, além do mais se enquadra no perfil de comprador, o [perfil de usuário](../personas) mais básico | Cadastro |

#### L12 - **Conta ativa**

| Classificação | Noção  | Impacto | Sinônimos |
| ------------- | ------ | ------- | :-------: |
| Estado | Uma conta ativa é passiva de ser visualizada e um usuário possuindo uma conta com essa característica é capaz de realizar todas as funcionalidades do sistema relacionadas ao seu perfil, exceto para o [perfil de moderador](../personas) | Uma conta ativa pode se tornar [desativada](#l12-conta-desativada) com o desejo do usuário | - |

#### L13 - **Conta desativada**

| Classificação | Noção  | Impacto | Sinônimos |
| ------------- | ------ | ------- | :-------: |
| Estado | Uma conta só pode ser desativada pelo usuário vinculado (exceto para o [perfil de moderador](../personas)). Uma conta desativada não é passiva de ser visualizada e um usuário possuindo uma conta com essa característica não é capaz de realizar as funcionalidades do sistema | Uma conta permanece desativada até que o usuário a ative | - |

## Referências Bibliográficas

> SAMPAIO, Julio; FRANCO, Ana. "A strategy for Conceptual Model Acquisition". Departamento de informática, Pontíficia Universidade Católica, Rio de Janeiro.

## Versionamento

| Versão | Data       | Modificação                    | Motivo | Autor         |
| ------ | ---------- | -------------------------------| ------ | ------------- |
| [1.0](../../../../versoes/lexico/1.0/) | 11/02/2021 | Criação do documento de léxico e adição algumas palavras | - | Rhuan Queiroz |
| [1.1](../../../../versoes/lexico/1.1/) | 13/02/2021 | Adição de motivo na tabela de versionamento | Melhorar o versionamento dos documentos | Igor Paiva |
| [1.2](../../../../versoes/lexico/1.2/) | 13/02/2021 | Adição da palavra "usuário" ao léxico | Definir os usuários do sistema | Igor Paiva |
| [1.3](../../../../versoes/lexico/1.3/) | 16/02/2021 | Adição do link para o arquivo de personas a partir da palavra "perfil de usuário" | Facilitar a navegação entre os documentos | Thiago Guilherme |
| [1.4](../../../../versoes/lexico/1.4/) | 16/02/2021 | Adição das palavras: "Invalidar", "Anúncio válido", "Anúncio inválido" ao léxico | Melhorar a compreensão dos termos do projeto | Igor Paiva, Marcelo Victor e Thiago Lopes |
| [1.5](../../../../versoes/lexico/1.5/) | 17/02/2021 | Mudança na classificação dos léxicos L9 e L10 | Correções nas classificações | Igor Paiva, Marcelo Victor e Thiago Lopes |
| 2.0 | 22/03/2021 | Adição das palavras: "conta", "conta ativa" e "conta desativada" | Aprimorar a compreensão dos termos do projeto | Igor Paiva, Rhuan Queiroz, Thiago Lopes |
