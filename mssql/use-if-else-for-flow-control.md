---
title: "Usar `IF ... ELSE` para controle de fluxo no SQL Server"
author: "bw3sley"
slug: "use-if-else-for-flow-control"
tags:
  - mssql
  - tsql
  - control-flow
created_at: "2022-08-15"

---

# Usar `IF ... ELSE` para controle de fluxo no SQL Server

`IF ... ELSE` executa blocos diferentes conforme resultado de uma expressão booleana.

```sql
IF (@Numero > 5)
BEGIN
  PRINT 'Tudo certo!'
END
ELSE
BEGIN
  PRINT 'Deu ruim'
END
```
