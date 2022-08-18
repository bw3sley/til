---
title: "Iniciar `useState` com valor compatível evita estado `undefined`"
author: "bw3sley"
slug: "initialize-usestate-with-compatible-value-to-avoid-undefined-state"
tags:
  - react
  - state
  - hooks
created_at: "2026-07-09"

---

# Iniciar `useState` com valor compatível evita estado `undefined`

Se o estado vai guardar um array, comece com um array vazio. Isso mantém o tipo consistente desde a primeira renderização e evita checagens extras para `undefined`.

```tsx
const [people, setPeople] = useState<Person[]>(); // Person[] | undefined
const [users, setUsers] = useState<Person[]>([]); // Person[]
```
