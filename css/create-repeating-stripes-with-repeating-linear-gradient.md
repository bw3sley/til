---
title: "Criar listras repetidas com `repeating-linear-gradient()`"
author: "bw3sley"
slug: "create-repeating-stripes-with-repeating-linear-gradient"
tags:
  - css
  - gradients
  - background
created_at: "2022-03-23"

---

# Criar listras repetidas com `repeating-linear-gradient()`

`repeating-linear-gradient()` repete o mesmo padrão de cor ao longo do fundo. Bom para criar listras, grades ou texturas simples sem imagem.

```css
.box {
  background-image: repeating-linear-gradient(
    45deg,
    rgba(128, 128, 128, 0.2) 0px,
    rgba(128, 128, 128, 0.2) 10px,
    transparent 10px,
    transparent 20px
  );
}
```
