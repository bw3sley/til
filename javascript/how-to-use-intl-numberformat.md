# Intl.NumberFormat

O objeto **Intl.NumberFormat** permite formatar números de forma sensível ao idioma e região.

Certifique-se de especificar o idioma desejado no argumento `locales`.

## Moeda

Você pode usar o argumento `options` para personalizar o resultado e formatar números como moeda.

Exemplo:

```javascript
const numero = 123456.789;

console.log(new Intl.NumberFormat('pt-BR', { style: 'currency', currency: 'BRL' }).format(numero));
```

## Unidades

Também é possível formatar números com unidades específicas utilizando o argumento `options`.

Exemplo:

```javascript
const numero = 123456.789;

console.log((numero).toLocaleString('pt-BR', {
  style: 'unit',
  unit: 'centimeter',
}));
```

## Referências

- [📄 Documentação MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl/NumberFormat/NumberFormat#options)