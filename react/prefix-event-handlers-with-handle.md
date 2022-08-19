---
title: "Prefixar handlers de evento com `handle`"
author: "bw3sley"
slug: "prefix-event-handlers-with-handle"
tags:
  - react
  - events
  - naming
created_at: "2026-07-09"

---

# Prefixar handlers de evento com `handle`

Usar `handle` no nome da função deixa explícito que ela será usada como resposta a um evento da interface.

```tsx
function handleSubmit() {}
function handleDeletePost() {}

<button onClick={handleSubmit}>Salvar</button>
```
