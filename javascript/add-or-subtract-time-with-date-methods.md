---
title: "Usar métodos de `Date` para avançar ou voltar datas"
author: "bw3sley"
slug: "add-or-subtract-time-with-date-methods"
tags:
  - javascript
  - dates
created_at: "2026-07-05"

---

# Usar métodos de `Date` para avançar ou voltar datas

Ao copiar uma data e usar `setDate()` ou `setFullYear()`, dá para calcular datas futuras ou passadas sem biblioteca externa.

```js
const future = new Date(today);
future.setDate(future.getDate() + 30);
console.log(future);
// data atual + 30 dias
```
