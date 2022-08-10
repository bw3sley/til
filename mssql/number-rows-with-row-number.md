---
title: "Usar `ROW_NUMBER()` para numerar linhas no resultado"
author: "bw3sley"
slug: "number-rows-with-row-number"
tags:
  - mssql
  - window-functions
created_at: "2026-07-05"

---

# Usar `ROW_NUMBER()` para numerar linhas no resultado

`ROW_NUMBER()` atribui numeração sequencial conforme ordenação definida no `OVER`.

```sql
SELECT ROW_NUMBER() OVER (ORDER BY CustomerName) AS ID, Customer.*
FROM Customer;
```
