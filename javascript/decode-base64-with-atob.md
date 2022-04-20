---
title: "Usar `atob()` para decodificar string em Base64"
author: "bw3sley"
slug: "decode-base64-with-atob"
tags:
  - javascript
  - base64
created_at: "2026-07-05"

---

# Usar `atob()` para decodificar string em Base64

`atob()` converte uma string Base64 de volta para conteúdo decodificado no navegador.

```js
const decoded = atob("SGVsbG8sIHdvcmxk=");
// "Hello, world"
```
