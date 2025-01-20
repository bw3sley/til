---
title: "Usar `<datalist>` para sugerir valores em um input"
author: "bw3sley"
slug: "use-datalist-for-input-suggestions"
tags:
  - html
  - forms
  - datalist
created_at: "2022-03-30"

---

# Usar `<datalist>` para sugerir valores em um input

`<datalist>` fornece sugestões para um `<input>`, mas ainda permite que a pessoa digite um valor fora da lista.

```html
<input list="cidades" name="cidade">
<datalist id="cidades">
  <option value="São Paulo">
  <option value="Rio de Janeiro">
</datalist>
```

// O input passa a sugerir "São Paulo" e "Rio de Janeiro".
