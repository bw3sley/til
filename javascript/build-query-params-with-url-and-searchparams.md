---
title: "Montar query params com `URL` e `searchParams`"
author: "bw3sley"
slug: "build-query-params-with-url-and-searchparams"
tags:
  - javascript
  - url
  - fetch
created_at: "2026-07-09"

---

# Montar query params com `URL` e `searchParams`

Criar a URL com `new URL()` evita concatenação manual de string e facilita adicionar parâmetros opcionais antes do `fetch`.

```js
async function fetchTransaction(query) {
  const url = new URL("http://localhost:3333/transactions");

  if (query) {
    url.searchParams.append("q", query);
  }

  const response = await fetch(url);
  const data = await response.json();

  console.log(data);
}
```
