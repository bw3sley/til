---
title: "Preferir atualizações imutáveis ao mudar estado no React"
author: "bw3sley"
slug: "prefer-immutable-updates-when-changing-state"
tags:
  - react
  - state
  - immutability
created_at: "2026-07-05"

---

# Preferir atualizações imutáveis ao mudar estado no React

No React, o ideal é criar um novo valor em vez de mutar o anterior. Isso facilita detectar mudança e recalcular a interface corretamente.

```tsx
setComments((state) => {
  return [...state, newComment];
});
```

Em vez de mutar `state`, o código cria um novo array.
