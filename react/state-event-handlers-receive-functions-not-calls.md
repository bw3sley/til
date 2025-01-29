---
title: "Passar função para evento em vez de executar na renderização"
author: "bw3sley"
slug: "state-event-handlers-receive-functions-not-calls"
tags:
  - react
  - events
  - state
created_at: "2022-06-28"

---

# Passar função para evento em vez de executar na renderização

Eventos esperam uma função. Se você chamar a função direto no JSX, ela roda durante a renderização e não no clique.

```tsx
<button onClick={handleLikeComment} />
<button onClick={handleLikeComment()} />
```

Só primeira versão passa callback corretamente.
