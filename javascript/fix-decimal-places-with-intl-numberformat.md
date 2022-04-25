---
title: "Usar `Intl.NumberFormat` para fixar casas decimais"
author: "bw3sley"
slug: "fix-decimal-places-with-intl-numberformat"
tags:
  - javascript
  - intl
  - numbers
created_at: "2026-07-05"

---

# Usar `Intl.NumberFormat` para fixar casas decimais

Com `minimumFractionDigits` e `maximumFractionDigits`, `Intl.NumberFormat` formata inteiros e decimais com mesma quantidade de casas.

```js
new Intl.NumberFormat("pt-BR", {
  minimumFractionDigits: 2,
  maximumFractionDigits: 2,
}).format(1234);
// 1.234,00
```
