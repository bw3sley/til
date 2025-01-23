---
title: "Usar `JSON.parse(JSON.stringify(...))` para clone profundo simples"
author: "bw3sley"
slug: "deep-clone-with-json-parse-and-stringify"
tags:
  - javascript
  - objects
  - clone
created_at: "2022-04-21"

---

# Usar `JSON.parse(JSON.stringify(...))` para clone profundo simples

Para objetos simples, `JSON.parse(JSON.stringify(...))` cria cópia profunda separando referências aninhadas.

```js
const copy = JSON.parse(JSON.stringify(original));
copy.details.city = "New York";

console.log(original.details.city);
// "Wonderland"

console.log(copy.details.city);
// "New York"
```

Não funciona bem com `Date`, funções ou referências circulares.
