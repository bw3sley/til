---
title: "Usar `*=` para selecionar atributo que contém texto"
author: "bw3sley"
slug: "use-attribute-selector-to-match-part-of-value"
tags:
  - css
  - selectors
  - attributes
created_at: "2026-07-05"

---

# Usar `*=` para selecionar atributo que contém texto

O seletor de atributo com `*=` encontra elementos cujo valor do atributo contém uma substring em qualquer posição.

Isso é útil quando o valor do atributo varia, mas ainda carrega um trecho previsível que você pode usar como alvo do estilo.

```css
[data-type*="produto"] {
  border: 1px solid #333;
}
```
