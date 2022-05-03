# Formatar um Decimal com um Número Fixo de Dígitos

O objeto `Intl.NumberFormat` é uma maneira confiável de formatar números de forma compatível com a internacionalização (i18n). Ele está disponível no Node e em todos os navegadores modernos.

Se eu quiser formatar um número que espero conter decimais, posso fazer isso configurando um formatador usando o estilo `decimal`.

```javascript
const locale = "pt-BR";
const options = {
  style: "decimal",
};

const formatter = new Intl.NumberFormat(locale, options);

console.log(formatter.format(1234))
//=> 1.234
console.log(formatter.format(1234.5678))
//=> 1.234,568
```

Por causa do meu local (`pt-BR`), ele adiciona um ponto para separar as milhar e uma vírgula para os decimais. Por padrão, ele formata com três casas decimais, excluindo as casas decimais se o número for inteiro.

Se eu quiser especificar um número fixo de casas decimais, mesmo para números inteiros, posso usar as opções `minimumFractionDigits` e `maximumFractionDigits`.

```javascript
const locale = "pt-BR";
const options = {
  style: "decimal",
  minimumFractionDigits: 2,
  maximumFractionDigits: 2,
};

const formatter = new Intl.NumberFormat(locale, options);

console.log(formatter.format(1234))
//=> 1.234,00
console.log(formatter.format(1234.5678))
//=> 1.234,57
```

Aqui, ele inclui o `.00` no número inteiro e corta os números com mais de 2 casas decimais, arredondando conforme necessário.

## Referências

- [💡 jbranchaud/til](https://github.com/jbranchaud/til)