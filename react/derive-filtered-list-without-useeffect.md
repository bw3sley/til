---
title: "Derivar lista filtrada sem `useEffect`"
author: "bw3sley"
slug: "derive-filtered-list-without-useeffect"
tags:
  - react
  - useeffect
  - state
created_at: "2026-07-09"

---

# Derivar lista filtrada sem `useEffect`

Se um valor pode ser calculado a partir do estado atual, prefira derivar isso direto na renderização. Usar `useEffect` para sincronizar outro estado nesse caso só duplica a fonte de verdade.

```tsx
const [list, setList] = useState<string[]>([]);
const [filter, setFilter] = useState("");

const filteredList = list.filter((item) => item.includes(filter));
```
