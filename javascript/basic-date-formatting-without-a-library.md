# Formatação Básica de Data Sem Uma Biblioteca

O JavaScript, nos navegadores modernos, possui uma API de Internacionalização (Internationalization API) que, entre outras coisas, oferece utilitários para formatação de datas. Você pode começar a usá-la sem a necessidade de importar uma biblioteca pesada de formatação de datas.

Aqui está um objeto `Date`:

```javascript
> const now = new Date();
> now
Tue Nov 19 2019 16:23:43 GMT-0600 (Central Standard Time)
```

A formatação padrão com essa API já é um bom começo:

```javascript
> Intl.DateTimeFormat('pt-BR').format(now)
"19/11/2019"
```

Também existem várias opções para formatação mais avançada. Aqui está a opção `dateStyle` com os quatro possíveis valores:

```javascript
> Intl.DateTimeFormat('pt-BR', { dateStyle: "full" }).format(now)
"terça-feira, 19 de novembro de 2019"
> Intl.DateTimeFormat('pt-BR', { dateStyle: "long" }).format(now)
"19 de novembro de 2019"
> Intl.DateTimeFormat('pt-BR', { dateStyle: "medium" }).format(now)
"19 de nov. de 2019"
> Intl.DateTimeFormat('pt-BR', { dateStyle: "short" }).format(now)
"19/11/19"
```

## Referências

- [💡 jbranchaud/til](https://github.com/jbranchaud/til)