---
title: "Página com `noindex` não deve ser bloqueada no `robots.txt`"
author: "bw3sley"
slug: "noindex-page-must-not-be-blocked-by-robots-txt"
tags:
  - seo
  - robots-txt
  - noindex
created_at: "2026-07-04"

---

# Página com `noindex` não deve ser bloqueada no `robots.txt`

Se a página estiver bloqueada no `robots.txt`, o crawler pode nem chegar a ler a diretiva `noindex`.

Para essa estratégia funcionar, a URL precisa continuar acessível ao bot.

```html
<meta name="robots" content="noindex">
```
