# Interfaces com o Mesmo Nome São Mescladas

Aqui está a declaração de uma interface em TypeScript.

```typescript
interface Person {
  name: string;
}
```

E se eu adicionar uma declaração de interface separada com o mesmo nome, `Person`?

```typescript
interface Person {
    age: number;
}
```

TypeScript realiza a mesclagem de declarações. Portanto, os tipos das duas interfaces serão combinados. Assim, uma variável do tipo `Person` pode ter um `name` e uma `age`.

```typescript
const person: Person = {
    age: 22,
    name: 'Bob'
};
```

Veja um [exemplo ao vivo](https://www.typescriptlang.org/play?ssl=12&ssc=2&pln=5&pc=1#code/JYOwLgpgTgZghgYwgAgArQM4HsTIN4BQyxyIcAthAFzIZhSgDmBAvgQaJLIiulNrkIlkcRtVIBXcgCNordghx1kAB0w4afAcgC8+IiVHiATMYA0B4mUo0A5ACEs02-IJr+OAHRGgA) no TS Playground.

Isso é diferente de como as declarações de tipo de objeto lidam com isso. Se eu tentar definir dois `type`s separados com o mesmo nome, isso resultaria em um erro de tipo.

## Referências

- [💡 jbranchaud/til](https://github.com/jbranchaud/til)
- [Typescript](https://www.typescriptlang.org/docs/handbook/declaration-merging.html#merging-interfaces)