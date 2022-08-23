---
title: "Usar `memo` para pular render quando props não mudam"
author: "bw3sley"
slug: "use-react-memo-to-skip-rerender-when-props-do-not-change"
tags:
  - react
  - memo
  - performance
created_at: "2026-07-09"

---

# Usar `memo` para pular render quando props não mudam

`memo` reaproveita o último resultado do componente quando as props continuam iguais. Em componente simples, a comparação pode custar mais que a renderização, então vale mais em partes pesadas da interface.

```tsx
function SearchFormComponent() {
  return <form>{/* ... */}</form>;
}

export const SearchForm = memo(SearchFormComponent);
```
