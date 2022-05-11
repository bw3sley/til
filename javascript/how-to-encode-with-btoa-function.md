# BTOA

O método `btoa()` cria uma string ASCII codificada em Base64 a partir de uma string binária (ou seja, uma string em que cada caractere é tratado como um byte de dados binários).

Você pode usar esse método para codificar dados que podem causar problemas de comunicação, transmiti-los e, em seguida, usar o método `atob()` para decodificar os dados novamente. Por exemplo, é possível codificar caracteres de controle, como valores ASCII de 0 a 31.

Exemplo:

```javascript
const dadosCodificados = btoa("Hello, world");
```

## Referências

- [📄 Documentação MDN](https://developer.mozilla.org/en-US/docs/Web/API/btoa)