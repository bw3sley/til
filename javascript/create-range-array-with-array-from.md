---
title: "Usar `Array.from()` para criar array de `1` até `N`"
author: "bw3sley"
slug: "create-range-array-with-array-from"
tags:
  - javascript
  - arrays
created_at: "2026-07-05"

---

# Usar `Array.from()` para criar array de `1` até `N`

`Array.from()` com função de mapeamento gera sequências numéricas sem loop manual.

```js
const arr = Array.from({ length: 10 }, (_, i) => i + 1);
// [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```
