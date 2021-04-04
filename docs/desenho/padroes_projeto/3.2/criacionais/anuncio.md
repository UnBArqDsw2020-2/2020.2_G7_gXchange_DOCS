# Builder - Criação do anúncio

## Problema

<p style="text-indent: 20px; text-align: justify">
Como criar um anúncio, que é um objeto complexo, cheio de atributos que podem variar dado o contexto de criação?
</p>

## Solução

<p style="text-indent: 20px; text-align: justify">
Uma solução seria construir o Anúncio, que é um objeto complexo, em etapas. Sendo assim passa a existir um componente Builder para o anúncio enquanto que vai haver outro componente que estará utilizando o Builder. Dessa forma, é possível manter a coesão dos componentes, sendo que um componente será responsável pela parte de interface de usuário enquanto outro componente será responsável pelas etapas de construção do objeto Anúncio.
</p>

<p style="text-indent: 20px; text-align: justify">
Essa abordagem apresenta vantagens por encapsular as lógicas de construção do objeto fora do componente de interface. E dependendo como é feito, no caso do front-end, em conjunto com a store o builder consegue ser acessível a outros componentes que precisem alterar o Anúncio em construção.
</p>

<p style="text-indent: 20px; text-align: justify">
Dentro da estrutura de Builder, há a classe diretora, no caso qualquer classe que precise utilizar o builder será considerada a diretora.
</p>

## Código

``` typescript
class OfferBuilder {
    private offer: Offer; // O tipo Offer refere-se ao tipo Anúncio

    public getProduct(): Offer{
      // Retorna o produto no final do processo
      // Pode também retornar erros referentes a regras de negócio
      // Por exemplo, o anúncio deve ter ao menos uma foto.
      return Offer;
    }

    public addPhoto(img: Image): void {
      // Adiciona uma imagem ao objeto Anúncio
    }

    public removePhoto (img_id: number): void {
      // Remove uma das fotos do anúncio
    }

    public setPrice(price: number): void {
      // Remove uma das fotos do anúncio
    }

    public setType(type: number): void {
      // Muda o tipo do anúncio, se é de troca, venda ou ambos
    }

    public setCondition(condition: number) {
      // Muda a condição da mídia do jogo a que se refere o anúncio
    }

    public setPlatform(platform: string) {
      // Muda a plataforma do jogo a que se refere o anúncio
    }

    // E outros métodos de configuração do objeto no builder
    ...
}
```

## Versionamento

| Versão | Data       | Modificação               | Motivo | Autor         |
| ------ | ---------- | ------------------------- | ------ | ------------- |
| 1.0 | 04/04/2021 | Criação do documento | Listar o problema de criação de um novo anúncio | Todos os integrantes |
