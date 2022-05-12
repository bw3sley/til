# String.prototype.padStart() | padEnd()

Os métodos `padStart()` e `padEnd()` preenchem a string até que ela atinja o comprimento desejado.

Exemplo:

```javascript
"abc".padStart(10);         // "       abc"
"abc".padStart(10, "foo");  // "foofoofabc"

"abc".padEnd(10);           // "abc       "
"abc".padEnd(10, "foo");    // "abcfoofoof"
```

## Referências

- [📄 Documentação MDN — padStart()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/padStart)  
- [📄 Documentação MDN — padEnd()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/padEnd)