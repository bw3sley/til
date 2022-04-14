# Acessando argumentos de uma função

O objeto `arguments` está disponível dentro de qualquer função JavaScript. Ele é um objeto semelhante a um array que contém todos os argumentos passados para a função. Mesmo que nem todos os argumentos estejam declarados na assinatura da função, eles ainda podem ser acessados via o objeto `arguments`.

```javascript
function argTest(one) {
  console.log(one);
  console.log(arguments);
  console.log(arguments[1]);
}

argTest(1);
// 1
// [1]
// undefined

argTest(1, 'two', true);
// 1
// [1, 'two', true]
// 'two'
```

## Referências

- [💡 jbranchaud/til](https://github.com/jbranchaud/til)

- Dorian Karter