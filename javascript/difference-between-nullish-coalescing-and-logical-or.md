# Diferença entre ?? e ||

Quando você precisa definir um valor padrão em JavaScript, pode usar os operadores `??` (Nullish Coalescing) ou `||` (Logical OR), mas eles funcionam de maneiras diferentes.

O operador `||` retorna o primeiro valor "truthy" que encontrar. Isso significa que ele considera "falsy" os seguintes valores: `false`, `0`, `''` (string vazia), `null`, `undefined` e `NaN`.

Exemplo com `||`:

```js
let a = 0;
let b = a || "default"; // b será "default" porque 0 é falsy
```

O operador `??` retorna o primeiro valor que **não** seja `null` ou `undefined`. É útil quando você deseja um valor padrão apenas nesses dois casos.

Exemplo com `??`:

```js
let a = 0;
let b = a ?? "default"; // b será 0 porque 0 não é null ou undefined
```

A diferença principal é que `||` trata qualquer valor "falsy" como motivo para retornar o segundo operando, enquanto `??` trata somente `null` e `undefined` dessa forma.

Exemplo de comparação:

```js
let a = "";
let b = a || "default";  // b será "default" porque "" é falsy
let c = a ?? "default";  // c será "" porque "" não é null ou undefined
```

Neste caso, `b` será `"default"` com `||`, mas `c` será `""` com `??` porque uma string vazia não é `null` nem `undefined`.