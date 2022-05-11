# Intl.DateTimeFormat

O objeto **Intl.DateTimeFormat** permite formatar datas e horários de forma sensível ao idioma e região.

## Sem usar Locales

Se você não especificar o `locale`, o formato padrão do sistema será utilizado.

Exemplo:

```javascript
const data = new Date(Date.UTC(2022, 11, 20, 3, 0, 0)); // ano, mês, dia, hora, minuto, segundos, ms

console.log(new Intl.DateTimeFormat().format(data));
```

## Usando Locales

Você pode especificar o idioma usando o argumento `locale`. Ao definir um locale, a data será formatada de acordo com as convenções dessa localidade.

Exemplo:

```javascript
const data = new Date(Date.UTC(2022, 11, 20, 3, 0, 0));

console.log(new Intl.DateTimeFormat("pt-BR").format(data));
```

## Opções

É possível personalizar o formato de data e hora usando o argumento `options`.

Exemplo:

```javascript
const data = new Date(Date.UTC(2012, 11, 20, 3, 0, 0, 200));

const opcoes = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' };

console.log(new Intl.DateTimeFormat('pt-BR', opcoes).format(data));
```

## Referências

- [📄 Documentação MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl/DateTimeFormat)