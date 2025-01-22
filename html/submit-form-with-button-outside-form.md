---
title: "Enviar formulário com botão fora do `<form>`"
author: "bw3sley"
slug: "submit-form-with-button-outside-form"
tags:
  - html
  - forms
  - buttons
created_at: "2022-03-30"

---

# Enviar formulário com botão fora do `<form>`

Um botão pode enviar um formulário mesmo fora dele. Basta usar `form` no botão apontando para o `id` do `<form>`.

```html
<form id="cadastro">
  <input type="text" name="name">
</form>

<button type="submit" form="cadastro">Enviar</button>
```
