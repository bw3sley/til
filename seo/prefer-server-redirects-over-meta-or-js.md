---
title: "Preferir redirecionamento via servidor em vez de meta ou JavaScript"
author: "bw3sley"
slug: "prefer-server-redirects-over-meta-or-js"
tags:
  - seo
  - redirects
  - http
created_at: "2026-07-04"

---

# Preferir redirecionamento via servidor em vez de meta ou JavaScript

Quando uma URL muda, o redirecionamento HTTP `3xx` no servidor costuma ser o sinal mais claro para navegador e crawler.

Meta refresh e JavaScript podem redirecionar também, mas não deveriam ser primeira escolha. Se a mudança for definitiva, prefira responder com `301`.
