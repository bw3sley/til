---
title: "`robots.txt` não remove página do Google"
author: "bw3sley"
slug: "robots-txt-does-not-remove-page-from-google"
tags:
  - seo
  - robots-txt
  - indexing
created_at: "2024-03-29"

---

# `robots.txt` não remove página do Google

Bloquear uma URL no `robots.txt` limita o rastreamento, mas isso não significa que a página será removida dos resultados do Google.

Quando o objetivo é impedir indexação, a diretiva correta é `noindex`.

```html
<meta name="robots" content="noindex">
```
