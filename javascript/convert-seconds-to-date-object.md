# Converter Segundos em um Objeto Date

Suponha que você tenha um número inteiro que representa o número de segundos desde a época Unix. Este é um formato razoavelmente comum que os sistemas utilizam para representar uma data.

Por exemplo, `1713350171` é uma _Data de Expiração_ que acabei de obter de uma API.

Mas como sabemos que data esse valor realmente representa e como podemos obter um objeto `Date` do JavaScript a partir desse valor?

O construtor `new Date()` pode gerar um objeto de data a partir de um número inteiro. No entanto, esse número não deve ser em segundos desde a época Unix. Veja o que obtemos aqui:

```javascript
> new Date(1713350171)
1970-01-20T19:55:50.171Z
```

Algo está errado. O número inteiro que você passa para `new Date()` precisa ser o _número de milissegundos_ desde a época Unix. Podemos corrigir isso multiplicando o valor em _segundos_ por `1000`.

```javascript
> new Date(1713350171 * 1000)
2024-04-17T10:36:11.000Z
```

Agora, além de conseguirmos ler a data, temos um objeto `Date` que podemos utilizar dentro do nosso programa.

Nota: se você executar `Date.now()`, o valor retornado será em milissegundos.

## Referências

- [💡 jbranchaud/til](https://github.com/jbranchaud/til)