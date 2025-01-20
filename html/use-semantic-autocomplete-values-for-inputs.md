---
title: "Usar valores semânticos no `autocomplete` de inputs"
author: "bw3sley"
slug: "use-semantic-autocomplete-values-for-inputs"
tags:
  - html
  - forms
  - autocomplete
created_at: "2022-04-06"

---

# Usar valores semânticos no `autocomplete` de inputs

O atributo `autocomplete` não aceita só `on` e `off`. Ele também aceita valores semânticos que ajudam o navegador a preencher tipos específicos de dado, como identidade, contato, endereço, pagamento e autenticação.

```html
<input name="name" autocomplete="name">
<input name="email" autocomplete="email">
<input name="address" autocomplete="street-address">
<input name="password" type="password" autocomplete="current-password">
<input name="otp" autocomplete="one-time-code">
```
