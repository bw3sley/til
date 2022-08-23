---
title: "Usar `useMemo` para cachear cálculo derivado"
author: "bw3sley"
slug: "use-usememo-to-cache-derived-calculation"
tags:
  - react
  - hooks
  - performance
created_at: "2026-07-09"

---

# Usar `useMemo` para cachear cálculo derivado

`useMemo` guarda o resultado de um cálculo entre renderizações até as dependências mudarem. Ele não impede render por si só, mas evita recalcular ou recriar referências sem necessidade.

```tsx
const summary = useMemo(() => {
  return transactions.reduce(
    (accumulator, transaction) => {
      if (transaction.type === "income") {
        accumulator.income += transaction.price;
        accumulator.total += transaction.price;
      } else {
        accumulator.outcome += transaction.price;
        accumulator.total -= transaction.price;
      }

      return accumulator;
    },
    {
      income: 0,
      outcome: 0,
      total: 0,
    },
  );
}, [transactions]);
```
