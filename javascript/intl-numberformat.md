# Intl.NumberFormat
The **Intl.NumberFormat** object enables language-sensitive number formatting.

Make sure to specify the language that you want to use inside the `locales`. 

## Currency
You need to use some the `options` argument to customize the result.

Eg: 
```
const numbers = 123456.789;

console.log(new Intl.NumberFormat('pt-BR', { style: 'currency', currency: 'BRL' }).format(numbers));
```

## Units
You need to use some the `options` argument to customize the result.

Eg: 
```
const numbers = 123456.789;

console.log((numbers).toLocaleString('pt-BR', {
  style: 'unit',
  unit: 'centimeter',
}));
```

For an exhaustive list of options, see the [Intl.NumberFormat()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl/NumberFormat/NumberFormat#options) constructor page.