# ATOB

A função `atob()` decodifica uma string que foi codificada usando Base64. Você pode usar o método `btoa()` para codificar e transmitir dados que podem causar problemas de comunicação e, em seguida, usar o método `atob()` para decodificar os dados novamente. Por exemplo, é possível codificar, transmitir e decodificar caracteres de controle, como valores ASCII de 0 a 31.

Exemplo:

```javascript
const dadosDecodificados = atob(dadosCodificados); // decodifica a string
```

## Referências

- [📄 Documentação MDN](https://developer.mozilla.org/en-US/docs/Web/API/atob)