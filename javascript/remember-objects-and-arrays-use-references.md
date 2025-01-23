---
title: "Lembrar que objetos e arrays são atribuídos por referência"
author: "bw3sley"
slug: "remember-objects-and-arrays-use-references"
tags:
  - javascript
  - arrays
  - objects
created_at: "2022-05-04"

---

# Lembrar que objetos e arrays são atribuídos por referência

Ao atribuir um objeto ou array para outra variável, você não cria uma cópia. As duas variáveis passam a apontar para a mesma referência na memória.

Por isso, uma mutação feita por uma delas também aparece na outra.

```js
const a = [{ name: "Alice" }];
const b = a;

console.log(a[0].name); // "Alice"

b[0].name = "Bob";

console.log(a[0].name); // "Bob"
console.log(b[0].name); // "Bob"
```
