# BEGIN...END

A declaração **BEGIN...END** é usada para definir um bloco de instruções. Um bloco de instruções consiste em um conjunto de comandos SQL que são executados em conjunto. Esse bloco também é conhecido como *batch*.

Em outras palavras, se os comandos SQL são frases, a declaração **BEGIN...END** permite agrupá-las em parágrafos.

Exemplo:

```sql
BEGIN
    SELECT
        Products.Id,
        Products.Name
    FROM Products
    WHERE
        Products.Price > 100000;

    IF @@ROWCOUNT = 0
        PRINT 'Nenhum produto com preço maior que 100000 foi encontrado';
END
```

## Referências

- [📄 Documentação Microsoft — BEGIN...END (Transact-SQL)](https://learn.microsoft.com/en-us/sql/t-sql/language-elements/begin-end-transact-sql)