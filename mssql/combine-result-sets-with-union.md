---
title: "Usar `UNION` para combinar resultados de múltiplos `SELECT`s"
author: "bw3sley"
slug: "combine-result-sets-with-union"
tags:
  - mssql
  - union
created_at: "2026-07-05"

---

# Usar `UNION` para combinar resultados de múltiplos `SELECT`s

`UNION` junta resultados compatíveis e remove duplicados. `UNION ALL` mantém duplicados.

```sql
SELECT City, Country FROM Customers WHERE Country = 'Germany'
UNION
SELECT City, Country FROM Suppliers WHERE Country = 'Germany';
```
