---
title: 'Usar `translate="no"` para impedir tradução automática'
author: "bw3sley"
slug: "prevent-translation-with-html-translate-attribute"
tags:
  - html
  - attributes
  - i18n
created_at: "2022-03-28"

---

# Usar `translate="no"` para impedir tradução automática

O atributo `translate` controla se o conteúdo pode ser traduzido por ferramentas automáticas. Use `no` quando nomes ou termos não devem mudar.

```html
<p translate="no">Nome da marca</p>
```

// Ferramentas automáticas devem preservar "Nome da marca" sem traduzir.
