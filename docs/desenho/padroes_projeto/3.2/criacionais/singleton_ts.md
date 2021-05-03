# Singleton - Typescript

## Problema

<p style="text-indent: 20px; text-align: justify">
É um padrão da comunidade que uma aplicação só pode possuir uma única <em>store</em>. Então isso faz com que a <em>store</em> seja um <em>singleton</em> na arquitetura da aplicação.
</p>

## Solução

<p style="text-indent: 20px; text-align: justify">
É criada uma única <em>store</em> e é fornecido um ponto de acesso global a ela, para componentes React ela é passada a partir de <em>high-order components</em> e para arquivos Typescript normais ela pode ser acessada importando a <em>store</em> exportada no arquivo da <em>store</em> e usando as funções fornecidas.
</p>

## Código

### Store do front-end gXchange

``` typescript
import { configureStore } from '@reduxjs/toolkit';
import GlobalModalSlice from './store/GlobalModal';

const store = configureStore({
  reducer: {
    globalModalState: GlobalModalSlice,
  },
});

export type StoreState = ReturnType<typeof store.getState>;
export type StoreDispatch = typeof store.dispatch;

export default store;
```

### Store passada para a aplicação

``` typescript
import React from 'react';
import ReactDOM from 'react-dom';
import { Provider } from 'react-redux';
import App from './App';
import store from './store';

ReactDOM.render(
  <React.StrictMode>
    <Provider store={store}>
      <App />
    </Provider>
  </React.StrictMode>,
  document.getElementById('root'),
);
```

### Acessando e mudando a store em um componente React

``` typescript
import React from 'react';
import { useDispatch, useSelector } from 'react-redux';
import { StoreState } from '../../store';

const GlobalModal: React.FC = () => {
  const dispatch = useDispatch();

  const { open, title, type, content } = useSelector(
    (store: StoreState) => store.globalModalState,
  );

  const handleClose = () => {
    dispatch(closeModal());
  };

  // ....... MAIS LÓGICA DO COMPONENTE
};
```

### Acessando e mudando a store em um arquivo React

``` typescript
import store, { StoreState } from '../../store';
import { reducerAction } from '../../store/Reducer';

const Component: React.FC = () => {
  const state = store.getState();

  store.dispatch(reducerAction());
};
```

## Referências

>"How can I use the Redux store in non-component files?". Redux. MDN Web Docs. Disponível em: https://redux.js.org/faq/code-structure#how-can-i-use-the-redux-store-in-non-component-files. Acesso em: 04 abr. 2021.

## Versionamento

| Versão | Data       | Modificação               | Motivo | Autor         |
| ------ | ---------- | ------------------------- | ------ | ------------- |
| 1.0 | 04/04/2021 | Criação do documento | Documentar o uso do padrão singleton na store do front-end  | Todos os integrantes |
