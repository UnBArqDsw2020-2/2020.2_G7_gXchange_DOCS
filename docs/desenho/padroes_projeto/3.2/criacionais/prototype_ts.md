# Prototype - Typescript

## Problema

<p style="text-indent: 20px; text-align: justify">
Especificar os tipos de objetos a serem criados usando uma instância-protótipo e criar novos objetos pela cópia desse protótipo.
</p>

## Solução

<p style="text-indent: 20px; text-align: justify">
A linguagem programação Javascript e Typescript são linguagens com orientação a objetos baseadas em <em>prototype</em>. Nelas, é possível criar instâncias de objetos copiando as coisas comuns entre o tipo de objeto. Em Javascript e Typescript essa cópia é efeita automaticamente para os objetos comuns da linguagem. Mas também é fornecida uma maneira de criar seus <em>prototypes</em>.
</p>

## Código

### Exemplo de um objeto comum

**Script**:

``` typescript
const obj = {};

console.log('obj: ', obj);
```

**Output**:

![Output 1](../../../../../../../assets/gofs/prototype01.png)

### Exemplo de um objeto com a cadeia de prototype de objetos normais e uma própria

**Script**:

``` typescript
const customPrototype = {
  prop1: 'prop1',
  prop2: 'prop2',
  prop3: 'prop3',
  prop4: 'prop4',
};

const customObj = Object.create(customPrototype);

console.log('customObj  : ', customObj);
```

**Output**:

![Output 2](../../../../../../../assets/gofs/prototype02.png)

### Exemplo de um objeto customizado sem a cadeia de prototype de objetos normais

**Script**:

``` typescript
const customProto = Object.create(null);

customProto.prop1 = 'prop1';
customProto.prop2 = 'prop2';
customProto.prop3 = 'prop3';
customProto.prop4 = 'prop4';

const customObj = Object.create(customProto);

console.log('customObj  : ', customObj);
```

**Output**:

![Output 3](../../../../../../../assets/gofs/prototype03.png)

## Referências

>"Object.create()". MDN Web Docs. Disponível em: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Object/create. Acesso em: 04 abr. 2021.

>"Prototypal Inheritance in JavaScript". Douglas Crockford. Disponível em: http://crockford.com/javascript/prototypal.html. Acesso em: 04 abr. 2021.

## Versionamento

| Versão | Data       | Modificação               | Motivo | Autor         |
| ------ | ---------- | ------------------------- | ------ | ------------- |
| 1.0 | 04/04/2021 | Criação do documento | Documentar o uso do padrão prototype na linguagem Typescript | Todos os integrantes |
