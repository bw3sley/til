---
title: "Usar Context API quando props só atravessam vários componentes"
author: "bw3sley"
slug: "use-context-api-when-props-only-cross-many-components"
tags:
  - react
  - context
  - props
created_at: "2026-07-09"

---

# Usar Context API quando props só atravessam vários componentes

Se uma prop existe só para atravessar vários níveis até chegar no componente que realmente usa o valor, isso já é sinal de prop drilling. Nesse caso, `Context` reduz a passagem intermediária.

Uma forma simples é criar o contexto em um arquivo próprio e envolver a aplicação no `main.tsx`.

```tsx
// contexts/cycles-context.tsx
import { createContext } from "react";

type CyclesContextData = {
  activeCycle: number;
  setActiveCycle: (value: number) => void;
};

export const CyclesContext = createContext({} as CyclesContextData);

// main.tsx
import { useState } from "react";
import { App } from "./App";
import { CyclesContext } from "./contexts/cycles-context";

function Root() {
  const [activeCycle, setActiveCycle] = useState(0);

  return (
    <CyclesContext.Provider value={{ activeCycle, setActiveCycle }}>
      <App />
    </CyclesContext.Provider>
  );
}

// Countdown.tsx
import { useContext } from "react";
import { CyclesContext } from "./contexts/cycles-context";

function Countdown() {
  const { activeCycle } = useContext(CyclesContext);
  return <h1>{activeCycle}</h1>;
}
```
