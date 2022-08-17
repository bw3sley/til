---
title: "Usar `as const` para preservar valores literais em objetos"
author: "bw3sley"
slug: "use-as-const-to-preserve-literal-values-in-objects"
tags:
  - typescript
  - literals
created_at: "2026-07-09"

---

# Usar `as const` para preservar valores literais em objetos

`as const` evita que o TypeScript alargue valores como `"yellow-500"` para `string`. Isso mantém o objeto com tipos literais mais específicos.

```ts
const STATUS_COLOR = {
  yellow: "yellow-500",
  blue: "blue-500",
} as const;

type StatusColor = typeof STATUS_COLOR[keyof typeof STATUS_COLOR];
// "yellow-500" | "blue-500"
```
