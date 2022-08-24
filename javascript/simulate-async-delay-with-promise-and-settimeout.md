---
title: "Simular atraso assíncrono com `Promise` e `setTimeout`"
author: "bw3sley"
slug: "simulate-async-delay-with-promise-and-settimeout"
tags:
  - javascript
  - async
  - promise
created_at: "2026-07-09"

---

# Simular atraso assíncrono com `Promise` e `setTimeout`

Uma `Promise` com `setTimeout` cria uma espera artificial no fluxo assíncrono. Isso ajuda a testar loading, submit ou buscas demoradas.

```js
async function handleSearchTransactions(data) {
  await new Promise((resolve) => setTimeout(resolve, 2000));

  console.log(data);
}
```
