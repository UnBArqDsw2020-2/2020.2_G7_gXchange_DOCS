# Léxico

## Introdução

<p style="text-indent: 20px; text-align: justify">
Léxico trata-se de uma técnica que procura descrever os símbolos de uma linguagem, o
principal objetivo a ser perseguido pelos Engenheiros de Requisitos é a identificação de palavras ou
frases peculiares ao meio social da aplicação sob estudo. Cada simbolo é descrito com noção e
impacto.
</p>

## Metodologia

Utilizaremos como base o modelo de tabela abaixo:

### **Símbolo**

| Classificação       | Noção     | Impacto   | Sinônimos |
| ------------------- | --------- | --------- | --------- |
| Objeto/Estado/Verbo | Denotação | Conotação | Opcional  |

## Léxicos

#### L1 - **Anúncio**

| Classificação | Noção                                                            | Impacto                                         | Sinônimos  |
| ------------- | ---------------------------------------------------------------- | ----------------------------------------------- | ---------- |
| Objeto        | Referente a publicação de um jogo disponível para troca ou venda | Usuário visualiza rapidamente diversos anúncios | Publicação |

#### L2 - **Vender**

| Classificação | Noção                              | Impacto                                                                   | Sinônimos |
| ------------- | ---------------------------------- | ------------------------------------------------------------------------- | --------- |
| Verbo         | Forma de um usuário vender um jogo | O vendedor ao vender um de seus jogos permite ao comprador receber o jogo | -         |

#### L3 - **Trocar**

| Classificação | Noção                              | Impacto                                                                           | Sinônimos |
| ------------- | ---------------------------------- | --------------------------------------------------------------------------------- | --------- |
| Verbo         | Forma de um usuário trocar um jogo | Dois usuários entram em acordo e trocam entre si as mídias físicas dos seus jogos | Escambo   |

#### L4 - **Jogo**

| Classificação | Noção                                                            | Impacto                                              | Sinônimos    |
| ------------- | ---------------------------------------------------------------- | ---------------------------------------------------- | ------------ |
| Objeto        | Um jogo digital em mídia física geralmente utilizado em consoles | Podem ser publicados para serem vendidos ou trocados | Mídia Física |

#### L5 - **Avaliar**

| Classificação | Noção                                              | Impacto                                                | Sinônimos |
| ------------- | -------------------------------------------------- | ------------------------------------------------------ | --------- |
| Verbo         | Ato de um usuário ser avaliado por outros usuários | O usuário avaliado terá sua nota de avaliação alterada | -         |

#### L6 - **Reportar**

| Classificação | Noção                                                        | Impacto                                                                | Sinônimos |
| ------------- | ------------------------------------------------------------ | ---------------------------------------------------------------------- | --------- |
| Verbo         | Ato de um usuário reportar uma publicação e/ou outro usuário | O usuário reportado ou publicação reportada será levado para avaliação | Denunciar |

#### L7 - **Usuário**

| Classificação | Noção | Impacto | Sinônimos |
| ------------- | ------| ------- | --------- |
| Objeto | Qualquer pessoa que esteja utilizando o sistema, de acordo com o perfil de usuário definido | O usuário pode publicar, comprar, trocar [jogos](/lexico/#l4-jogo) | Comprador, vendedor, moderador |

## Referências Bibliográficas

> SAMPAIO, Julio; FRANCO, Ana. "A strategy for Conceptual Model Acquisition". Departamento de informática, Pontíficia Universidade Católica, Rio de Janeiro.

## Versionamento

| Versão | Data       | Modificação                    | Motivo | Autor         |
| ------ | ---------- | -------------------------------| ------ | ------------- |
| [1.0](/versoes/lexico/1.0/) | 11/02/2021 | Criação do documento de léxico e adição algumas palavras | - | Rhuan Queiroz |
| [1.1](/versoes/lexico/1.1/) | 13/02/2021 | Adição de motivo na tabela de versionamento | Melhorar o versionamento dos documentos | Igor Paiva |
| 1.2 | 13/02/2021 | Adição da palavra "usuário" ao léxico | Definir os usuários do sistema | Igor Paiva |
