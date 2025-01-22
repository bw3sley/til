---
title: "Usar `Intl.DateTimeFormat` para formatar datas sem biblioteca"
author: "bw3sley"
slug: "format-dates-with-intl-datetimeformat"
tags:
  - javascript
  - intl
  - dates
created_at: "2022-04-26"

---

# Usar `Intl.DateTimeFormat` para formatar datas sem biblioteca

`Intl.DateTimeFormat` já resolve formatação local de datas no navegador e no Node, sem depender de biblioteca externa.

```js
const now = new Date();

Intl.DateTimeFormat("pt-BR", { dateStyle: "long" }).format(now);
// 19 de novembro de 2019
```
