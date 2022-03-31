# Stored Procedures
SQL Server stored procedures are used to group one or more Transact-SQL statements into logical units. The stored procedure is stored as a named object in the SQL Server Database Server.

When you call a stored procedure for the first time, SQL Server creates an execution plan and stores it in the cache. In the subsequent executions of the stored procedure, SQL Server reuses the plan to execute the stored procedure very fast with reliable performance.

## Creating a Stored Procedure
o create a stored procedure that wraps this query, you use the ``CREATE PROCEDURE`` statement.

Eg:
```
    CREATE PROCEDURE ProductList
        @Product VARCHAR(20)
    AS
    BEGIN
        SELECT 
            Product.ProductName, 
            Product.Price

        FROM Product

        WHERE Product.ProductName = @Product

        ORDER BY 
            Product.ProductName
    END
    GO
```

## Executing a Stored Procedure
To execute a stored procedure, you use the ``EXECUTE`` or ``EXEC`` statement followed by the name of the stored procedure:

Eg:
```
    EXECUTE ProductList;
```

## Modifying a Stored Procedure
To modify an existing stored procedure, you use the ``ALTER PROCEDURE`` statement.

Eg:
```
    ALTER PROCEDURE ProductList
        @Product VARCHAR(20)
    AS
    BEGIN
        SELECT 
            Product.ProductName, 
            Product.Price,
            Product.,

        FROM Product

        WHERE Product.ProductName = @Product

        ORDER BY 
            Product.ProductName
    END
    GO
```

## Deleting a Stored Procedure
To delete a stored procedure, you use the ``DROP PROCEDURE`` or ``DROP PROC`` statement.

Eg:
```
    DROP PROCEDURE ProductList;
```