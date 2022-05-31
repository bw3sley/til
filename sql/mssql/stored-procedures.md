# Stored Procedures

As **Stored Procedures** no SQL Server são usadas para agrupar uma ou mais instruções Transact-SQL em unidades lógicas. A procedure armazenada é salva como um objeto nomeado no servidor de banco de dados SQL Server.

Quando você executa uma **stored procedure** pela primeira vez, o SQL Server cria um plano de execução e o armazena em cache. Em execuções subsequentes, o SQL Server reutiliza esse plano, resultando em uma execução mais rápida e com desempenho confiável.

## Criando uma Stored Procedure

Para criar uma **stored procedure**, utilize o comando `CREATE PROCEDURE`.

Exemplo:

```sql
CREATE PROCEDURE ProductList
    @Product VARCHAR(20)
AS
BEGIN
    SELECT 
        Product.ProductName, 
        Product.Price
    FROM Product
    WHERE Product.ProductName = @Product
    ORDER BY Product.ProductName;
END
GO
```

---

## Executando uma Stored Procedure

Para executar uma **stored procedure**, use o comando `EXECUTE` ou `EXEC` seguido pelo nome da procedure:

Exemplo:

```sql
EXECUTE ProductList;
```

---

## Modificando uma Stored Procedure

Para modificar uma **stored procedure** existente, use o comando `ALTER PROCEDURE`.

Exemplo:

```sql
ALTER PROCEDURE ProductList
    @Product VARCHAR(20)
AS
BEGIN
    SELECT 
        Product.ProductName, 
        Product.Price
    FROM Product
    WHERE Product.ProductName = @Product
    ORDER BY Product.ProductName;
END
GO
```

---

## Deletando uma Stored Procedure

Para excluir uma **stored procedure**, utilize o comando `DROP PROCEDURE` ou `DROP PROC`.

Exemplo:

```sql
DROP PROCEDURE ProductList;
```

---

## Referências

- [📄 Documentação Microsoft — Stored Procedures (Transact-SQL)](https://learn.microsoft.com/en-us/sql/relational-databases/stored-procedures/stored-procedures-database-engine)