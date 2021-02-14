# Análise de riscos

## Introdução

<p style="text-indent: 20px; text-align: justify">
O planejamento da gerência de risco é o processo de definir como conduzir as atividades de gerência de risco para um projeto.
</p>

## Estrutura analítica de Riscos

![EAR](assets/ear.png)

### Organizacional

- Priorização: são riscos relacionados a erros de priorização, que geram impasses relacionados a entregas.

- Habilidades individuais: São riscos relacionadaos as habilidades dos integrantes da equipe, tanto *hard-skills* quanto *soft-skills*.

- Recursos: são riscos relacionados a recursos de tempo e dinheiro.

### Técnico

- Definição do escopo: são riscos relacionados ao escopo do produto e mal defini-lo acarreta problemas nas entregas.

- Tecnologia: são riscos relacionados às tecnologias envolvidas no projeto.

- Definição dos requisitos: são riscos relacionados a especificação e escrita dos requisitos.

- Infraestrutura: são riscos relacionados a infraestrura para o desenvolvimento do projeto. 

### Gerência de projeto

- Estimativas: são relacionados a estimativa dos prazos de tarefas e podem gerar impasses na entrega.

- Planejamento: são riscos relacionados ao planejamento do projeto.

- Controle: são riscos relacionados ao controle de riscos.

- Execução: são riscos relacionados a como as tarefas e o planejamento será executado.

### Qualidade

- Portabilidade: são riscos relacionados sobre a acessibilidade do projeto em diversos dispositivos com acesso a internet.

- Usabilidade: são riscos relacionados a facilidade e intuitividade da interface do projeto.

- Eficiência: são os riscos relacionados ao produto administrar melhor os recursos, impacta diretamente no desempenho.

- Segurança: são riscos relacionados a segurança e preservação de dados dos usuários do sistema.

## Análise Quantitativa dos riscos

### Probabilidade de riscos e impactos

<p style="text-indent: 20px; text-align: justify">
Essas escalas podem ser usadas para avaliar tanto ameaças quanto oportunidades, interpretando as definições de impacto como negativas para as ameaças, e positivas para as oportunidades.
</p>

<p style="text-indent: 20px; text-align: justify">
Definimos a probabilidade como sendo a chance de uma escala ocorrer. Também definimos a unidade de tempo baseada em sprints de 7 dias.
</p>

| Escala | Probabilidade |
|:-:|:-:|
| Muito Alta | 61-100% |
| Alta | 31-60% |
| Média | 16-30% |
| Baixa | 6-15% |
| Muito Baixa | <5% |


| Escala | Impacto | Tempo | Descrição |
|:-:|:-:|:-:|--|
| Muito baixo | <5% | 1 dia | Impacto pequeno em funções secundárias |
| Baixo | 6-15% | 2-4 dias | Impacto pequeno nas funcionalidades gerais |
| Médio | 16-30% | 1 sprint | Algum impacto nas principais funcionalidades |
| Alto | 31-50% | 2 sprints | Impacto significante nas funcionalidade gerais |
| Muito Alto | 51-80% | 4 sprints | Impacto extremamente significante nas funcionalidades | gerais |

### Matriz de probabilidade e impacto - Prioridade

<iframe height="380px" width="100%" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSd_dZ4ZoB35vzz9yXwua2z-2ZxH5sM7Y2SW9M4AG1ghp18D1eRPmBi1BAcox2OYrTksnk2Lt-tw7gH/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false"></iframe>

[Link para a planilha](https://docs.google.com/spreadsheets/d/1EpUkZ90QRISpWAHJeTkk2KQbCKVyE606x8nKwAPlMzE/edit?usp=sharing)

## Referências

> "Project Management Body of Knowledge 6th edition". Project Management Institute, 2017.

## Versionamento

| Versão | Data       | Modificação          | Motivo | Autor         |
| ------ | ---------- | -------------------- | ------ | ------------- |
|  1.0   | 14/02/2021 | Criação do documento | Fazer uma análise de risco do projeto | Igor Paiva, Rhuan Queiroz, Marcelo Victor, Thiago Lopes e Washington Bispo |
