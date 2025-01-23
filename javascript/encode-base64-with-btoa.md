---
title: "Usar `btoa()` para codificar string em Base64"
author: "bw3sley"
slug: "encode-base64-with-btoa"
tags:
  - javascript
  - base64
created_at: "2022-04-22"

---

# Usar `btoa()` para codificar string em Base64

`btoa()` gera representação Base64 de uma string no navegador.

Isso é útil para transportar texto em formatos que aceitam melhor ASCII, mas não serve como criptografia.

```js
const encoded = btoa("Hello, world");
// "SGVsbG8sIHdvcmxk="
```
