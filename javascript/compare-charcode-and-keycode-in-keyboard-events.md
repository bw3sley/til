---
title: "Comparar `charCode` e `keyCode` em eventos de teclado"
author: "bw3sley"
slug: "compare-charcode-and-keycode-in-keyboard-events"
tags:
  - javascript
  - dom
  - keyboard
created_at: "2026-07-05"

---

# Comparar `charCode` e `keyCode` em eventos de teclado

Em eventos de teclado, `keypress` costuma carregar código de caractere, enquanto `keydown` e `keyup` tendem a expor mais o código da tecla.

```js
window.addEventListener("keypress", (e) => {
  console.log(e.charCode, e.keyCode);
});
// 97 97
```
