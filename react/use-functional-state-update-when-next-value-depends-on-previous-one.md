---
title: "Usar atualização funcional quando novo estado depende do anterior"
author: "bw3sley"
slug: "use-functional-state-update-when-next-value-depends-on-previous-one"
tags:
  - react
  - state
  - closures
created_at: "2022-06-30"

---

# Usar atualização funcional quando novo estado depende do anterior

Quando próximo valor depende do estado atual, prefira callback no setter para evitar usar valor desatualizado.

```tsx
function handleLikeComment() {
  setLikeCount((state) => {
    return state + 1;
  });
}
```
