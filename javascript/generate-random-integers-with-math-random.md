---
title: "Usar `Math.floor()` com `Math.random()` para inteiro aleatório"
author: "bw3sley"
slug: "generate-random-integers-with-math-random"
tags:
  - javascript
  - math
created_at: "2022-04-28"

---

# Usar `Math.floor()` com `Math.random()` para inteiro aleatório

`Math.random()` gera decimal entre `0` e `1`. Para inteiro, combine com `Math.floor()`.

```js
function getRandomInt(max) {
  return Math.floor(Math.random() * Math.floor(max));
}

getRandomInt(10);
// 0 a 9
```
