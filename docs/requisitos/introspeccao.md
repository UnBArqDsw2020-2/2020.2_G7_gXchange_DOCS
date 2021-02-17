# Instrospecção

## Introdução

<p style="text-indent: 20px; text-align: justify">
O método de introspecção consiste em se colocar no papel dos usuários do sistema e imaginar o que os mesmos gostariam e/ou necessitariam que o sistema cumprisse para suprir as suas necessidades, e também suas características. Neste processo, utilizaremos <a href="/personas">personas</a> para tornar o processo de identificação e interpretação dos usuários-alvo do sistema mais fácil.
</p>

## Requisitos

<div>
<table>
<tr>
<th style="text-align: center">Número</th>
<th>Personas</th>
<th>Requisito</th>
<th>Tipo</th>
</tr>

<tr>
<td style="text-align: center">1</td>
<td style="text-align: justify">O vendedor e comprador devem ser capazes de se cadastrarem usando sua conta do Google</td>
<td><a href="/personas/#persona-1-thomas-araujo-souza">Thomas</a> e <a href="/personas/#persona-2-carlos-macedo-dos-santos">Carlos</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">2</td>
<td style="text-align: justify">O vendedor e comprador devem ser capazes de se cadastrarem usando sua conta do Facebook</td>
<td><a href="/personas/#persona-1-thomas-araujo-souza">Thomas</a> e <a href="/personas/#persona-2-carlos-macedo-dos-santos">Carlos</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">3</td>
<td style="text-align: justify">O vendedor e comprador devem ser capazes de criarem uma conta do sistema</td>
<td><a href="/personas/#persona-1-thomas-araujo-souza">Thomas</a> e <a href="/personas/#persona-2-carlos-macedo-dos-santos">Carlos</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">4</td>
<td style="text-align: justify">O comprador deve ser capaz de <a href="/lexico/#l6-reportar">reportar</a> um anúncio feito por um vendedor</td>
<td><a href="/personas/#persona-1-thomas-araujo-souza">Thomas</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">5</td>
<td style="text-align: justify">O comprador deve ser capaz de <a href="/lexico/#l5-avaliar">avaliar</a> um vendedor após realizar uma troca ou compra</td>
<td><a href="/personas/#persona-1-thomas-araujo-souza">Thomas</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">6</td>
<td style="text-align: justify">O vendedor deve ser capaz de <a href="/lexico/#l5-avaliar">avaliar</a> um comprador após a realização de uma compra ou troca</td>
<td><a href="/personas/#persona-2-carlos-macedo-dos-santos">Carlos</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">7</td>
<td style="text-align: justify">O comprador deve ser capaz de visualizar as informações dos anúncios</td>
<td><a href="/personas/#persona-1-thomas-araujo-souza">Thomas</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">8</td>
<td style="text-align: justify">O vendedor deve ser capaz de cadastrar um novo anúncio</td>
<td><a href="/personas/#persona-2-carlos-macedo-dos-santos">Carlos</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">9</td>
<td style="text-align: justify">O comprador, após ter interagido com vendedor, deve ser capaz de reportar o vendedor</td>
<td><a href="/personas/#persona-1-thomas-araujo-souza">Thomas</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">10</td>
<td style="text-align: justify">O vendedor, após ter interagido com comprador, deve ser capaz de reportar o comprador</td>
<td><a href="/personas/#persona-2-carlos-macedo-dos-santos">Carlos</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">11</td>
<td style="text-align: justify">O sistema deve fornecer um sistema de mensagens para o comprador e o vendedor interagirem</td>
<td><a href="/personas/#persona-1-thomas-araujo-souza">Thomas</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">12</td>
<td style="text-align: justify">O sistema deve salvar um anúncio com as seguintes características: nome do(s) jogo(s), plataforma, condição, foto(s), informações do vendedor, localização, preço e descrição</td>
<td><a href="/personas/#persona-1-thomas-araujo-souza">Thomas</a> e <a href="/personas/#persona-2-carlos-macedo-dos-santos">Carlos</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">13</td>
<td style="text-align: justify">O sistema deve persistir as mensagens entre comprador e vendedor de um determinado anúncio por 7 dias após o fechamento desse anúncio, contanto que não haja nenhuma denúncia do comprador ou vendedor. Nesse caso, as mensagens deverão ser mantidas até a resolução da denúncia.</td>
<td><a href="/personas/#persona-1-thomas-araujo-souza">Thomas</a> e <a href="/personas/#persona-2-carlos-macedo-dos-santos">Carlos</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">14</td>
<td style="text-align: justify">O sistema deve manter as mensagens entre comprador e vendedor sem criptografia para que elas possam ser avaliadas no caso de denúncias</td>
<td><a href="/personas/#persona-3-sarah-brenda-santos">Sarah</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">15</td>
<td style="text-align: justify">O moderador deve ser capaz de <a href="/lexico/#l8-invalidar">invalidar</a> um anúncio</td>
<td><a href="/personas/#persona-3-sarah-brenda-santos">Sarah</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">16</td>
<td style="text-align: justify">O sistema deverá notificar o vendedor caso seu anúncio seja <a href="/lexico/#l8-invalidar">invalidado</a></td>
<td><a href="/personas/#persona-3-sarah-brenda-santos">Sarah</a> e <a href="/personas/#persona-2-carlos-macedo-dos-santos">Carlos</a></td>
<td>Funcional</td>
</tr>


<tr>
<td style="text-align: center">17</td>
<td style="text-align: justify">O sistema deve listar apenas <a href="/lexico/#l9-anuncio-valido">anúncios válidos</a></td>
<td><a href="/personas/#persona-1-thomas-araujo-souza">Thomas</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">18</td>
<td style="text-align: justify">O sistema deverá notificar o usuário quando um <a href="/lexico/#l1-anuncio">anúncio</a> que ele reportou for <a href="/lexico/#l8-invalidar">invalidado</a></td>
<td><a href="/personas/#persona-3-sarah-brenda-santos">Sarah</a> e <a href="/personas/#persona-1-thomas-araujo-souza">Thomas</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">19</td>
<td style="text-align: justify">O vendedor deve ser capaz de remover um <a href="/lexico/#l1-anuncio">anúncio</a></td>
<td><a href="/personas/#persona-2-carlos-macedo-dos-santos">Carlos</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">20</td>
<td style="text-align: justify">O vendedor deve ser capaz de editar um anúncio</td>
<td><a href="/personas/#persona-2-carlos-macedo-dos-santos">Carlos</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">21</td>
<td style="text-align: justify">O sistema deve notificar o comprador e vendedor de novas mensagens</td>
<td><a href="/personas/#persona-1-thomas-araujo-souza">Thomas</a> e <a href="/personas/#persona-2-carlos-macedo-dos-santos">Carlos</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">22</td>
<td style="text-align: justify">O moderador deve ser capaz de visualizar as denúncias de anúncios, vendedores e compradores</td>
<td><a href="/personas/#persona-3-sarah-brenda-santos">Sarah</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">23</td>
<td style="text-align: justify">O moderador deve ser capaz de banir um <a href="/lexico/#l7-usuario">usuário</a> (<a href="/requisitos/padroes/#a-ser-decidido"><strong>a ser decidido</strong></a>)</td>
<td><a href="/personas/#persona-3-sarah-brenda-santos">Sarah</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">24</td>
<td style="text-align: justify">O sistema no momento de cadastro, deve pedir o consentimento dos usuários em relação aos termos de uso (<a href="/requisitos/padroes/#a-ser-decidido"><strong>a ser decidido</strong></a>)</td>
<td><a href="/personas/#persona-1-thomas-araujo-souza">Thomas</a>, <a href="/personas/#persona-2-carlos-macedo-dos-santos">Carlos</a> e <a href="/personas/#persona-3-sarah-brenda-santos">Sarah</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">25</td>
<td style="text-align: justify">O sistema deve salvar usuários com as seguintes características: nome, apelido (nome de usuário), email e senha</td>
<td><a href="/personas/#persona-1-thomas-araujo-souza">Thomas</a>, <a href="/personas/#persona-2-carlos-macedo-dos-santos">Carlos</a> e <a href="/personas/#persona-3-sarah-brenda-santos">Sarah</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">26</td>
<td style="text-align: justify">O comprador deve ser capaz de visualizar todos os anúncios válidos cadastrados</td>
<td><a href="/personas/#persona-1-thomas-araujo-souza">Thomas</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">27</td>
<td style="text-align: justify">O comprador deve ser capaz de filtrar os anúncios por suas informações</td>
<td><a href="/personas/#persona-1-thomas-araujo-souza">Thomas</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">28</td>
<td style="text-align: justify">O comprador deve ser capaz de personalizar a lista de anúncios exibidos para listarem apenas os que possuam tópicos de seu interesse</td>
<td><a href="/personas/#persona-1-thomas-araujo-souza">Thomas</a></td>
<td>Funcional</td>
</tr>

<tr>
<td style="text-align: center">29</td>
<td style="text-align: justify">O sistema deve informar o comprador e vendedor que as mensagens poderão ser verificadas em caso de denúncias</td>
<td><a href="/personas/#persona-3-sarah-brenda-santos">Sarah</a></td>
<td>Não funcional</td>
</tr>

<tr>
<td style="text-align: center">30</td>
<td style="text-align: justify">O sistema deve possibilitar uma navegabilidade ágil entre as funcionalidades (<a href="/requisitos/padroes/#a-ser-decidido"><strong>a ser decidido</strong></a>)</td>
<td><a href="/personas/#persona-1-thomas-araujo-souza">Thomas</a>, <a href="/personas/#persona-2-carlos-macedo-dos-santos">Carlos</a> e <a href="/personas/#persona-3-sarah-brenda-santos">Sarah</a></td>
<td>Não funcional</td>
</tr>

<tr>
<td style="text-align: center">31</td>
<td style="text-align: justify">A interface do sistema deverá possuir uma boa usabilidade (<a href="/requisitos/padroes/#a-ser-decidido"><strong>a ser decidido</strong></a>)</td>
<td><a href="/personas/#persona-2-carlos-macedo-dos-santos">Carlos</a>, <a href="/personas/#persona-1-thomas-araujo-souza">Thomas</a> e <a href="/personas/#persona-3-sarah-brenda-santos">Sarah</a></td>
<td>Não funcional</td>
</tr>

<tr>
<td style="text-align: center">32</td>
<td style="text-align: justify">O sistema de mensagens deve buscar novas mensagens em no máximo 5 segundos</td>
<td><a href="/personas/#persona-2-carlos-macedo-dos-santos">Carlos</a>, <a href="/personas/#persona-1-thomas-araujo-souza">Thomas</a></td>
<td>Não funcional</td>
</tr>

<tr>
<td style="text-align: center">33</td>
<td style="text-align: justify">O sistema deve funcionar em <i>smartphones</i></td>
<td><a href="/personas/#persona-2-carlos-macedo-dos-santos">Carlos</a>, <a href="/personas/#persona-1-thomas-araujo-souza">Thomas</a></td>
<td>Não funcional</td>
</tr>
</table>
</div>

## Referências

> Elicitação de Requisitos. PUC-RIO. Disponível em: http://www2.dbd.puc-rio.br/pergamum/tesesabertas/0521479_08_cap_02.pdf Acesso em: 20 set. 2020.

## Versionamento

| Versão | Data       | Modificação               | Motivo | Autor         |
| ------ | ---------- | ------------------------- | ------ | ------------- |
|  [1.0](../versoes/introspeccao/1.0.md)   | 16/02/2021 | Criação do documento de introspecção | Elicitar requisitos utilizando a técnica de instrospecção | Igor Paiva, Marcelo Victor e Thiago Lopes |
|  1.1  | 16/02/2021 | Correções gerais no documento de introspecção | Corrigir alguns problemas de rastreabilidade | Thiago Lopes |
