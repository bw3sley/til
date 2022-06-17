---
title: "Tipar array de objetos com interface no TypeScript"
author: "bw3sley"
slug: "type-arrays-of-objects-with-an-interface"
tags:
  - typescript
  - interfaces
created_at: "2026-07-05"

---

# Tipar array de objetos com interface no TypeScript

Uma interface ajuda a definir a estrutura esperada de cada item do array e mantém o acesso às propriedades tipado.

```ts
interface User {
  name: string;
  bio: string;
  age: number;
}

function sumAge(users: User[]) {
  let sum = 0;

  for (const user of users) {
    sum += user.age;
  }

  return sum;
}
```
