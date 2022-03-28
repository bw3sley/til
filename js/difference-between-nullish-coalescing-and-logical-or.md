# Diferença entre ?? e ||

## Introdução

Neste artigo, você aprenderá mais sobre a diferença entre os operadores `??` (Nullish Coalescing Operator) e `||` (Logical OR) em JavaScript. Ambos os operadores são usados para fornecer valores padrão, mas se comportam de maneira ligeiramente diferente, dependendo dos valores envolvidos.

## Como funciona?

O operador `||` (Logical OR) retorna o primeiro valor "truthy" que encontra na sequência de operandos. Se o primeiro operando for "falsy", ele retorna o segundo operando. Valores "falsy" incluem:

- `false`
- `0`
- `''` (string vazia)
- `null`
- `undefined`
- `NaN`

Exemplo de uso do operador `||`:

```js
let a = 0;
let b = a || "default"; // b será "default" porque 0 é um valor falsy
```

O operador `??` (Nullish Coalescing) retorna o primeiro valor que não é null ou undefined. Se o primeiro operando for null ou undefined, ele retorna o segundo operando.

Exemplo de uso do operador `??`:

```js
let a = 0;
let b = a ?? "default"; // b será 0 porque 0 não é null ou undefined
```

### Diferença Principal

A diferença crucial entre `||` e `??` é que o `||` considera qualquer valor "falsy" como motivo para retornar o segundo operando, enquanto o `??` considera apenas null ou undefined.

Exemplo de comparação entre `||` e `??`:

```js
let a = "";
let b = a || "default";  // b será "default" porque "" é falsy
let c = a ?? "default";  // c será "" porque "" não é null nem undefined
```

Neste exemplo, b obterá "default" usando `||`, mas c obterá "" usando `??` porque uma string vazia não é `null` nem `undefined`.

## Conclusão

Os operadores `??` e `||` são úteis para fornecer valores padrão em JavaScript, mas entender suas diferenças é crucial para evitar comportamentos inesperados em seu código. Use `||` quando quiser considerar todos os valores "falsy" como uma condição para retornar um valor padrão, e use `??` quando quiser tratar apenas `null` e `undefined` dessa forma. 