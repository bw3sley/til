---
title: "Multiplicar timestamp em segundos por `1000` antes de usar `Date`"
author: "bw3sley"
slug: "convert-unix-seconds-to-date"
tags:
  - javascript
  - dates
created_at: "2022-04-18"

---

# Multiplicar timestamp em segundos por `1000` antes de usar `Date`

`new Date()` espera milissegundos. Se a API retorna segundos Unix, multiplique por `1000` antes da conversão.

```js
new Date(1713350171 * 1000);
// 2024-04-17T10:36:11.000Z
```
