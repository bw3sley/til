---
title: "Interfaces com o mesmo nome são mescladas no TypeScript"
author: "bw3sley"
slug: "merge-interfaces-with-the-same-name"
tags:
  - typescript
  - interfaces
created_at: "2022-06-17"

---

# Interfaces com o mesmo nome são mescladas no TypeScript

Quando duas interfaces têm o mesmo nome, o TypeScript combina as propriedades das duas em um único tipo.

```ts
interface Person {
  name: string;
}

interface Person {
  age: number;
}

const person: Person = {
  age: 22,
  name: "Bob",
};
```

`Person` passa a exigir `name` e `age`.
