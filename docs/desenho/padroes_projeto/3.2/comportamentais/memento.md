# Memento - Estado anterior

## Problema

<p style="text-indent: 20px; text-align: justify">
Como restaurar um estado anterior da aplicação sem ferir o encapsulamento?
</p>

## Solução

<p style="text-indent: 20px; text-align: justify">
O useRef é uma ferramenta do React que salva um valor mutável, semelhante ao que se usa em campos de instâncias de classes. Com a diferença que ele retorna exatamente o objeto ref em que ele foi colocado.
</p>

<p style="text-indent: 20px; text-align: justify">
No código abaixo é mostrado como é possível retornar o valor do estado (state) do componente pai (Component) para o seu valor anterior através de um componente filho (ChildrenComponent), via prop, não violando o encapsulamento do estado.
</p>

## Código

``` typescript
const Component: React.FC = () => {
  const [state, setState] = useState(0);

  const usePrevious = (value) => {
    const ref = useRef();

    useEffect(() => {
      ref.current = value;
    });

    return ref.current;
  };

  const previousState = usePrevious(state);

  const returnToPreviousState = () => {
    setState(previousState);
  };

  return (
    <div>
      <ChildrenComponent goBack={returnToPreviousState}  />
    </div>
  );
};
```

## Versionamento

| Versão | Data       | Modificação               | Motivo | Autor         |
| ------ | ---------- | ------------------------- | ------ | ------------- |
| 1.0 | 04/04/2021 | Criação do documento | Descrever o componente useRef do React aplicado ao padrão Memento | Todos os integrantes |
