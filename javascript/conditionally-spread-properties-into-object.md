---
title: "Usar spread condicional para incluir propriedades em objeto"
author: "bw3sley"
slug: "conditionally-spread-properties-into-object"
tags:
  - javascript
  - objects
created_at: "2022-04-15"

---

# Usar spread condicional para incluir propriedades em objeto

Combinar `&&` com spread permite montar objetos dinâmicos sem mutação posterior.

```js
const person = {
  ...(includeAge && { age: 30 }),
  ...(includeName && { name: "Alice" }),
};
// { age: 30 }
```
