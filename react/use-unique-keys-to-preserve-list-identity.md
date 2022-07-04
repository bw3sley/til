---
title: "Usar `key` única para preservar identidade em listas"
author: "bw3sley"
slug: "use-unique-keys-to-preserve-list-identity"
tags:
  - react
  - lists
  - key
created_at: "2026-07-05"

---

# Usar `key` única para preservar identidade em listas

`key` ajuda o React a reconhecer quais itens continuam sendo os mesmos entre uma renderização e outra.

Na prática, isso evita recriação desnecessária de elementos que já existiam na lista.

```tsx
comments.map((comment) => {
  return <Comment key={comment.id} content={comment.content} />;
});
```