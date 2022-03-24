---
title: "Usar `:where()` para agrupar seletores sem aumentar especificidade"
author: "bw3sley"
slug: "use-where-to-group-selectors-with-zero-specificity"
tags:
  - css
  - selectors
  - specificity
created_at: "2026-07-05"

---

# Usar `:where()` para agrupar seletores sem aumentar especificidade

`:where()` agrupa seletores, mas sempre mantém especificidade `0`. Isso facilita criar estilos base que continuam fáceis de sobrescrever.

```css
:where(h1, h2, h3) {
  color: blue;
}
```

Diferença para `:is()`: `:where()` sempre mantém especificidade `0`, enquanto `:is()` usa a especificidade do seletor mais específico do grupo.
