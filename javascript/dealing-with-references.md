# Lidando com Referências no JavaScript

Em JavaScript, objetos e arrays são manipulados por **referência**. Isso significa que, ao atribuir um array ou objeto a uma nova variável, a nova variável não cria uma cópia dos dados, mas sim uma referência ao mesmo local na memória. Quando se trata de arrays complexos (arrays que contêm objetos ou outros arrays), qualquer alteração em um desses elementos afeta todos que compartilham a mesma referência.

### Edição por Referência

```javascript
const complexArray = [{ name: "Alice" }, { name: "Bob" }];

// Atribuindo o array a uma nova variável (por referência)
const newArray = complexArray;

// Modificando um objeto dentro do novo array
newArray[0].name = "Charlie";

console.log(complexArray[0].name); // "Charlie"
```

### Métodos que **não** Criam Cópia

Os métodos abaixo **modificam o array original**, porque não criam uma nova cópia, mas atuam diretamente sobre a referência:

- **push()**: Adiciona elementos ao final do array.
- **pop()**: Remove o último elemento do array.
- **shift()**: Remove o primeiro elemento do array.
- **unshift()**: Adiciona elementos no início do array.
- **splice()**: Adiciona, remove ou substitui elementos no array.
- **sort()**: Ordena os elementos do array.
- **reverse()**: Inverte a ordem dos elementos do array.

### Métodos que Criam Nova Cópia

Os métodos a seguir **criam uma nova cópia** do array e retornam o resultado sem modificar o array original:

- **slice()**: Retorna uma parte do array, criando uma nova cópia.
- **concat()**: Junta dois ou mais arrays, criando um novo array.
- **map()**: Cria um novo array com o resultado de uma função aplicada em cada elemento.
- **filter()**: Cria um novo array contendo apenas os elementos que passam em um teste.
- **reduce()**: Retorna um único valor, mas pode ser usado para construir novos arrays de maneira funcional.
- **flat()**: Retorna um novo array com todos os sub-arrays concatenados a ele.

### Exemplo de Uso de Métodos

```javascript
const arrayOriginal = [1, 2, 3, 4, 5];

// Criando uma cópia com slice()
const arrayCopia = arrayOriginal.slice();
arrayCopia.push(6);

console.log(arrayOriginal); // [1, 2, 3, 4, 5]
console.log(arrayCopia); // [1, 2, 3, 4, 5, 6]

// Modificando o array original com push()
arrayOriginal.push(6);
console.log(arrayOriginal); // [1, 2, 3, 4, 5, 6]
```