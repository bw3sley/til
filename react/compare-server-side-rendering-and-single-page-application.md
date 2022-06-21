---
title: "Diferenciar SSR de SPA no frontend"
author: "bw3sley"
slug: "compare-server-side-rendering-and-single-page-application"
tags:
  - react
  - rendering
created_at: "2026-07-05"

---

# Diferenciar SSR de SPA no frontend

No SSR, o servidor monta e devolve o HTML da rota já pronto. Na SPA, o backend tende a devolver dados e o frontend monta a interface no browser.

Na prática, SSR centraliza renderização no servidor. SPA facilita múltiplos clientes consumindo a mesma API, como web e mobile.

Exemplo: em uma SPA, o backend pode responder só com JSON para um app React e outro React Native.
