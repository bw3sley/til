---
title: "Usar `Intl.NumberFormat` para formatar números por locale"
author: "bw3sley"
slug: "format-numbers-with-intl-numberformat"
tags:
  - javascript
  - intl
  - numbers
created_at: "2026-07-05"

---

# Usar `Intl.NumberFormat` para formatar números por locale

`Intl.NumberFormat` formata números conforme idioma e região, inclusive moeda e unidade.

```js
new Intl.NumberFormat("pt-BR", {
  style: "currency",
  currency: "BRL",
}).format(123456.789);
// "R$ 123.456,79"
```
