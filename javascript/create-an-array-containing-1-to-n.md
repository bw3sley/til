# Criar um Array Contendo 1 até N

Você pode criar um array contendo uma sequência de números de 1 até N em JavaScript de forma simples usando o método `Array.from()`.

A função `Array.from()` permite criar arrays a partir de qualquer objeto que seja "iterável". Podemos usá-la para gerar um array de números consecutivos de 1 até N, da seguinte maneira:

```javascript
const n = 10;
const arr = Array.from({ length: n }, (_, i) => i + 1);
console.log(arr); // [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

Aqui, o método `Array.from()` cria um array com o tamanho especificado em `length: n`, e a função de mapeamento `( _, i ) => i + 1` gera valores de 1 até N.

## Referências

- [Questão do StackOverflow](https://stackoverflow.com/questions/3746725/how-to-create-an-array-containing-1-n/20066663#20066663)