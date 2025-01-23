---
title: "Usar `arguments` para acessar parâmetros extras de uma função"
author: "bw3sley"
slug: "access-extra-function-arguments-with-arguments"
tags:
  - javascript
  - functions
created_at: "2022-04-11"

---

# Usar `arguments` para acessar parâmetros extras de uma função

Dentro de funções não arrow, o objeto `arguments` expõe todos os valores recebidos, mesmo os que não aparecem na assinatura.

```js
function argTest(one) {
  console.log(one);
  console.log(arguments[1]);
}

argTest(1, "two");
// 1
// "two"
```
