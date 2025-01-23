# Incluir Pares Condicionalmente em um Objeto

Em JavaScript, ao criar um objeto, você pode querer incluir pares chave-valor com base em certas condições. Uma maneira eficiente de fazer isso é usando operadores lógicos ao definir as propriedades do objeto.

Aqui está um exemplo simples de como você pode condicionalmente adicionar pares chave-valor a um objeto:

```javascript
const includeAge = true;
const includeName = false;

const person = {
  ...(includeAge && { age: 30 }),
  ...(includeName && { name: 'Alice' }),
};

console.log(person); // { age: 30 }
```

Neste exemplo, usamos o operador lógico `&&` com a sintaxe de espalhamento `...` para incluir condicionalmente pares chave-valor no objeto `person`. Se `includeAge` for `true`, o par `age: 30` será incluído, caso contrário, será ignorado. O mesmo vale para `includeName`.

Essa abordagem é útil para criar objetos dinâmicos sem a necessidade de mutá-los posteriormente.