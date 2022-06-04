# sp_helptext

O procedimento armazenado **sp_helptext** no **SQL Server** é usado para exibir o código-fonte de objetos definidos pelo usuário, como **views**, **stored procedures**, **triggers** e **funções**. Ele permite visualizar o script T-SQL desses objetos diretamente pelo SQL Server Management Studio (SSMS) ou por comandos SQL.

---

## Sintaxe

```sql
sp_helptext [ 'nome_do_objeto' ];
```

- **nome_do_objeto**: O nome do objeto cujo código-fonte você deseja visualizar. Deve estar entre aspas simples.

---

## Exemplo de Uso

### Verificando o código-fonte de uma **Stored Procedure**:

```sql
sp_helptext 'usp_GetCustomerDetails';
```

Este comando retornará o código-fonte completo da stored procedure **usp_GetCustomerDetails**.

---

### Verificando o código-fonte de uma **View**:

```sql
sp_helptext 'vw_CustomerOrders';
```

Esse comando exibirá o script da view **vw_CustomerOrders**.

---

## Observações

- O **sp_helptext** exibe o código em várias linhas, cada uma retornada como uma linha separada no conjunto de resultados.
  
- Caso o objeto esteja em um esquema diferente do padrão (**dbo**), é necessário incluir o esquema no nome do objeto:

  ```sql
  sp_helptext 'schema_name.object_name';
  ```

- O **sp_helptext** **não** funciona com tabelas, apenas com objetos que possuem código-fonte T-SQL associado.

---

## Exemplo Completo

Suponha que você tenha criado a seguinte stored procedure:

```sql
CREATE PROCEDURE usp_GetCustomerDetails
    @CustomerID INT
AS
BEGIN
    SELECT 
        CustomerName, 
        Email, 
        Phone
    FROM Customers
    WHERE CustomerID = @CustomerID;
END;
GO
```

Para visualizar o código usando **sp_helptext**, execute:

```sql
sp_helptext 'usp_GetCustomerDetails';
```

Resultado esperado:

```
Text
--------------------------------------------------------------
CREATE PROCEDURE usp_GetCustomerDetails
    @CustomerID INT
AS
BEGIN
    SELECT 
        CustomerName, 
        Email, 
        Phone
    FROM Customers
    WHERE CustomerID = @CustomerID;
END
```

---

## Referências

- [📄 Documentação Microsoft — sp_helptext (Transact-SQL)](https://learn.microsoft.com/en-us/sql/relational-databases/system-stored-procedures/sp-helptext-transact-sql)