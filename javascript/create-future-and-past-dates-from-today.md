# Criar Datas Futuras e Passadas a Partir de Hoje

O objeto [`Date`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) nativo do JavaScript pode ser um pouco frustrante de trabalhar às vezes, mas é útil para realizar cálculos de datas. Você só precisa se familiarizar com algumas partes da API, e então poderá adicionar ou subtrair facilmente datas.

Aqui está a data de hoje:

```javascript
const today = new Date();
// Tue Jun 01 2022 ...
```

Vamos fazer uma cópia da data de hoje e avançar 30 dias no futuro:

```javascript
const future = new Date(today);
future.setDate(future.getDate() + 30);

console.log(future); // Thu Jun 31 2020 ...
```

Ou podemos retroceder alguns anos:

```javascript
const past = new Date(today);
past.setFullYear(past.getFullYear() - 4);
console.log(past); // Thu Jun 01 2018 ...
```

## Referências

- [💡 jbranchaud/til](https://github.com/jbranchaud/til)
- [Questão do StackOverflow](https://stackoverflow.com/questions/7908098/javascript-set-date-30-days-from-now/7908122#7908122)