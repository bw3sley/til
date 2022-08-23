---
title: "Usar `useCallback` para manter referência estável de função"
author: "bw3sley"
slug: "use-usecallback-to-keep-function-reference-stable"
tags:
  - react
  - hooks
  - performance
created_at: "2026-07-09"

---

# Usar `useCallback` para manter referência estável de função

`useCallback` guarda a mesma função entre renderizações enquanto as dependências não mudam. Isso faz diferença quando a função vira prop de componente com `memo` ou dependência de outro hook.

```tsx
const fetchTransactions = useCallback(async (query?: string) => {
  const response = await api.get("transactions", {
    params: {
      q: query,
    },
  });

  setTransactions(response.data);
}, []);
```
