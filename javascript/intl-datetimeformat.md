# Intl.DateTimeFormat
The **Intl.DateTimeFormat** object enables language-sensitive date and time formatting.

## Without using Locales
If you don't specify the `locale`, it'll use the default locale and default options.

Eg:
```
const date = new Date(Date.UTC(2022, 11, 20, 3, 0, 0)); // year, month, date, hour, minute, seconds, ms

console.log(new Intl.DateTimeFormat().format(date));
```

## Using Locales
Make sure to specify the language using the `locale` argument. When you choose one locale, it'll format the date to that.

Eg:
```
const date = new Date(Date.UTC(2022, 11, 20, 3, 0, 0));

console.log(new Intl.DateTimeFormat("pt-BR").format(date));
```

## Options
You can customize the date and time format using the `options` argument.

Eg:
```
const date = new Date(Date.UTC(2012, 11, 20, 3, 0, 0, 200));

const options = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' };

console.log(new Intl.DateTimeFormat('pt-BR', options).format(date));
```

For more information, see [Intl.DateTimeFormat](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl/DateTimeFormat) page.