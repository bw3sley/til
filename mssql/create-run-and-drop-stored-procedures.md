---
title: "Usar `CREATE`, `EXEC` e `DROP` com stored procedures"
author: "bw3sley"
slug: "create-run-and-drop-stored-procedures"
tags:
  - mssql
  - procedures
created_at: "2026-07-05"

---

# Usar `CREATE`, `EXEC` e `DROP` com stored procedures

No SQL Server, procedures são objetos nomeados que encapsulam consultas e lógica T-SQL reutilizável.

```sql
CREATE PROCEDURE ProductList
  @Product VARCHAR(20)
AS
BEGIN
  SELECT Product.ProductName, Product.Price
  FROM Product
  WHERE Product.ProductName = @Product;
END
```
