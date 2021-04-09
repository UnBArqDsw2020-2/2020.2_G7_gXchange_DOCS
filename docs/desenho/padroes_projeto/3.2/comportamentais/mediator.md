# Mediator - Django Views

## Problema

<p style="text-indent: 20px; text-align: justify">
Como mediar as Models, Serializers e Helpers.
</p>

## Solução

<p style="text-indent: 20px; text-align: justify">
As Views da API se comportam como mediadoras dos objetos do back-end. A lógica de comunicação pode ocorrer por meio das views, ao invés de deixar com que cada componente resolva por si próprio a comunicação com os outros.
</p>

## Modelagem

![Modelagem Mediator](../../../../../assets/gofs/modelos/mediator.png)

<a href="https://drive.google.com/file/d/1kcHc7-MB508hzRIlk8A-enkpcbqBO21l/view?usp=sharing" target="_blank" rel="noopener noreferrer">Link para a imagem</a>

## Código

```python
class CreateUser(generics.CreateAPIView):
    queryset = Person.objects.all() # Model
    serializer_class = PersonSerializer # Serializer
    lookup_field = ["email"]
```

outro exemplo

```python
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

| Versão | Data       | Modificação                                  | Motivo                                         | Autor                |
| ------ | ---------- | -------------------------------------------- | ---------------------------------------------- | -------------------- |
| 1.0    | 04/04/2021 | Criação do documento                         | Documentar a necessidade do mediador           | Todos os integrantes |
| 1.1    | 07/04/2021 | Alteração do título do documento             | O título estava divergente com o conteúdo      | Washington Bispo     |
| 1.2    | 08/04/2021 | Alteração da solução e inclusão da modelagem | Para que esteja documentado a modelagem do GOF | Marcelo Victor       |
