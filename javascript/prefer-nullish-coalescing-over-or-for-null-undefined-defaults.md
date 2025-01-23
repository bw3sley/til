---
title: "Usar `??` quando valor padrão deve cobrir só `null` e `undefined`"
author: "bw3sley"
slug: "prefer-nullish-coalescing-over-or-for-null-undefined-defaults"
tags:
  - javascript
  - operators
created_at: "2022-05-03"

---

# Usar `??` quando valor padrão deve cobrir só `null` e `undefined`

`||` troca qualquer valor falsy. `??` só cai no valor padrão quando o lado esquerdo é `null` ou `undefined`.

```js
0 || "default"; // "default"
0 ?? "default"; // 0
```
