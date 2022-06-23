---
title: "Evitar índice do array como `key` quando a ordem muda"
author: "bw3sley"
slug: "do-not-use-array-index-as-key-when-order-can-change"
tags:
  - react
  - lists
  - key
created_at: "2026-07-05"

---

# Evitar índice do array como `key` quando a ordem muda

Quando a lista muda de ordem, o índice deixa de representar a identidade real do item. Isso pode fazer o React recalcular ou reaproveitar elementos errados.

```tsx
comments.map((comment, index) => {
  return <Comment key={index} content={comment.content} />;
});
```

Se um comentário sair da posição `0` para `1`, a `key` muda mesmo sem ser um item novo.
