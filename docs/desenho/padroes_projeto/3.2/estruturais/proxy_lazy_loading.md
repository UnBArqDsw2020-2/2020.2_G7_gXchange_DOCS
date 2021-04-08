# Proxy - Lazy loading de imagens dos anúncios

## Problema

<p style="text-indent: 20px; text-align: justify">
Usuários com internet mais lentas podem sofrer problemas na renderização das imagens dos anúncios, além disso, o tempo para renderização pode causar <em>glitches</em> em que a página não fica corretamente formatada por que não está levando em conta o tamanho da imagem. 
</p>

## Solução

<p style="text-indent: 20px; text-align: justify">
A solução é usar outro objeto, um proxy (procurador), que funciona como um substituto temporário da imagem real. O proxy funciona exatamente como a imagem e toma conta da sua instanciação quando a mesma for necessária. Exemplo: Colocar uma imagem pré-renderizada com qualidade inferior enquanto a imagem com qualidade total é renderizada.
</p>

## Código

``` typescript
import React from 'react';
import { imgStyle } from './styles';
import PreloadImage from 'react-preload-image';

const Component: React.FC = () => {
  return (
    <div>
      <PreloadImage lazy src="anuncio.png" style={imgStyle} />
    </div>
  );
};
```

## Versionamento

| Versão | Data       | Modificação               | Motivo | Autor         |
| ------ | ---------- | ------------------------- | ------ | ------------- |
| 1.0 | 04/04/2021 | Criação do documento | Documentar o uso do Lazy loading | Todos os integrantes |
