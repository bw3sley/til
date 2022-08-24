---
title: "Usar curto-circuito com `&&` e `||` no JavaScript"
author: "bw3sley"
slug: "use-short-circuit-evaluation-with-and-and-or"
tags:
  - javascript
  - operators
created_at: "2026-07-09"

---

# Usar curto-circuito com `&&` e `||` no JavaScript

`||` para na primeira expressão truthy. `&&` para na primeira expressão falsy. Por isso, o lado direito nem sempre é avaliado.

```js
true || console.log("não roda");
false && console.log("não roda");
```
