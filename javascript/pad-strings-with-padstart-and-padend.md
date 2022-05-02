---
title: "Usar `padStart()` e `padEnd()` para completar strings"
author: "bw3sley"
slug: "pad-strings-with-padstart-and-padend"
tags:
  - javascript
  - strings
created_at: "2026-07-05"

---

# Usar `padStart()` e `padEnd()` para completar strings

`padStart()` adiciona preenchimento no início da string. `padEnd()` faz o mesmo no final.

```js
"abc".padStart(10, "foo");
// "foofoofabc"
"abc".padEnd(10, "foo");
// "abcfoofoof"
```
