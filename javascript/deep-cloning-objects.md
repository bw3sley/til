# Cópía profunda (Deep clone)

Em JavaScript, uma cópia profunda (deep clone) cria uma cópia completamente independente de um objeto ou array, incluindo todos os objetos ou arrays aninhados. Isso é diferente de uma cópia superficial, onde apenas o nível superior do objeto ou array é duplicado, e as referências internas permanecem inalteradas.

A cópia profunda é útil quando você precisa modificar um objeto ou array sem que as alterações afetem a estrutura original.

## Cópia Superficial vs. Cópia Profunda
- **Cópia superficial** (shallow copy) copia apenas o nível superior e mantém as referências internas.
- **Cópia profunda** (deep copy) copia todos os níveis de um objeto ou array, garantindo que as referências internas também sejam duplicadas.

### Exemplo de cópia profunda

Uma maneira simples de fazer uma cópia profunda de um objeto ou array é usando `JSON.parse()` e `JSON.stringify()`. No entanto, essa abordagem tem limitações (não funciona com funções, tipos especiais como `Date`, ou referências circulares).

```js
const original = { 
  name: "Alice", 
  details: { age: 30, city: "Wonderland" } 
};

const deepClone = JSON.parse(JSON.stringify(original));

deepClone.details.city = "New York";

console.log(original.details.city); // "Wonderland" (não foi alterado)
console.log(deepClone.details.city); // "New York"
```