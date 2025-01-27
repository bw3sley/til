---
title: "Usar `WHILE` para repetir lógica no SQL Server"
author: "bw3sley"
slug: "repeat-logic-with-while"
tags:
  - mssql
  - while
  - control-flow
created_at: "2022-08-10"

---

# Usar `WHILE` para repetir lógica no SQL Server

`WHILE` repete um bloco enquanto a condição continuar verdadeira. Pode ser combinado com `BREAK` e `CONTINUE`.

```sql
DECLARE @Counter INT = 0;

WHILE (@Counter <= 2)
BEGIN
  PRINT 'Contador = ' + CAST(@Counter AS VARCHAR);
  SET @Counter = @Counter + 1;
END
-- Contador = 0
-- Contador = 1
-- Contador = 2
```
