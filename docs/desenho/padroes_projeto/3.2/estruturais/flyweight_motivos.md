# FlyWeight - Motivos de denúncia

## Problema

<p style="text-indent: 20px; text-align: justify">
O problema consiste em: como padronizar os motivos de denúncia ao longo de todo o contexto da aplicação desde a API ao Front-end.
</p>

## Solução

<p style="text-indent: 20px; text-align: justify">
Uma solução possível seria utilizar uma abordagem semelhante a FlyWeight criando uma Model para conter o motivo da denúncia. De tal modo considera-se a denúncia como sendo o estado extrínseco, pois este é mutável, e os motivos de denúncia, que a príncipio eram referenciados como atributos, agora podem ser considerados como estado intrínseco a todas as denúncias.
</p>

<p style="text-indent: 20px; text-align: justify">
Fazendo assim a relação motivo de denúncia, tornar-se um relacionamento, deste modo, padronizam-se os motivos de denúncia. Inclusive podendo os usar para a criação de novas denúncias no Front-end pois como estão padronizadas, irão conter o texto da denúncia em si. Não somente, é possível alterar, inserir e até excluir (desde que os relacionamentos sejam trocados) motivos de denúncia em todo o contexto da aplicação. 
</p>

<p style="text-indent: 20px; text-align: justify">
Diferente do FlyWeight original este não acontece na memória RAM, e sim no Banco de Dados. Da mesma forma poupa armazenamento do banco, por não ter que ficar repetindo atributos de texto que muitas vezes são iguais. 
</p>

## Código

``` python
class Reason(models.Model):
    text = TextField(unique=True)
    pass

class Report(models.Model):
    creator = ForeignKey(User)
    reported = ForeignKey(User)
    reason = OneToOneField(Reason)
    date = DateField() 
    comment = TextField() # aqui deverá ir o comentário que servirá também como motivo caso seja marcado o motivo como 'outros'
```

também sendo necessária uma Serializer, que também pode se comportar como uma FlyWeightFactory, e uma View para que os motivos possam ser servidos pelo Back-end.

## Versionamento

| Versão | Data       | Modificação               | Motivo | Autor         |
| ------ | ---------- | ------------------------- | ------ | ------------- |
| 1.0 | 04/04/2021 | Criação do documento | Listar o problema de padronização dos motivos | Todos os integrantes |