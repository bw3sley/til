---
title: "Usar `:is()` para agrupar seletores com mesma regra"
author: "bw3sley"
slug: "use-is-to-group-selectors-with-shared-rules"
tags:
  - css
  - selectors
  - specificity
created_at: "2026-07-05"

---

# Usar `:is()` para agrupar seletores com mesma regra

`:is()` permite agrupar seletores em uma única regra. A especificidade continua valendo conforme o seletor mais específico dentro do grupo.

```css
:is(h1, h2, h3) {
  color: blue;
}
```

Diferença para `:where()`: `:is()` herda a especificidade do seletor mais específico do grupo, enquanto `:where()` sempre fica com especificidade `0`.
