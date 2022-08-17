---
title: "Usar `typeof` para inferir tipos a partir de valores já declarados"
author: "bw3sley"
slug: "use-typeof-to-infer-types-from-declared-values"
tags:
  - typescript
  - inference
  - zod
created_at: "2026-07-09"

---

# Usar `typeof` para inferir tipos a partir de valores já declarados

Quando o tipo depende de uma constante já criada, `typeof` leva esse valor para o sistema de tipos sem repetir a estrutura manualmente.

```ts
const newCycleFormValidationSchema = z.object({
  task: z.string(),
  minutesAmount: z.number(),
});

type NewCycleFormData = z.infer<typeof newCycleFormValidationSchema>;
```
