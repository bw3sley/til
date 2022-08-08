---
title: "Usar `BEGIN ... END` para agrupar instruções no SQL Server"
author: "bw3sley"
slug: "group-statements-with-begin-end"
tags:
  - mssql
  - tsql
created_at: "2026-07-05"

---

# Usar `BEGIN ... END` para agrupar instruções no SQL Server

`BEGIN ... END` delimita um bloco de instruções T-SQL executado como uma unidade lógica.

```sql
BEGIN
  SELECT Products.Id, Products.Name
  FROM Products
  WHERE Products.Price > 100000;
END
```
