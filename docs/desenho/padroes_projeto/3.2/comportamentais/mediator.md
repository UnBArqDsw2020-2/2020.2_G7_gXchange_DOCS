# Mediator - Django Views

## Problema

<p style="text-indent: 20px; text-align: justify">
Como mediar as Models, Serializers e Helpers.
</p>

## Solução

<p style="text-indent: 20px; text-align: justify">
As Views da API se comportam como mediadoras dos objetos do back-end.
</p>

## Código

``` python
class CreateUser(generics.CreateAPIView):
    queryset = Person.objects.all() # Model
    serializer_class = PersonSerializer # Serializer
    lookup_field = ["email"]
```

outro exemplo

``` python
class OfferPlatformListView(BaseFilterListView): # A Classe internament faz a mediação dos objetos que ela utiliza
    """
        View que lista todas os anúncios com uma dada plataforma
    """
    serializer_class = OfferSerializer # Utilizando a Serializer
    def get_queryset(self):
        platform = self.kwargs['platform'] 
        return Offer.objects.filter(platform=platform) # Utilizando a Model
```


## Versionamento

| Versão | Data       | Modificação               | Motivo | Autor         |
| ------ | ---------- | ------------------------- | ------ | ------------- |
| 1.0 | 04/04/2021 | Criação do documento | Documentar a necessidade do mediador | Todos os integrantes |
| 1.1 | 07/04/2021 | Alteração do título do documento | O título estava divergente com o conteúdo | Washington Bispo |
