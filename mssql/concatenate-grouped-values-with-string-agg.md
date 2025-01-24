---
title: "Usar `STRING_AGG()` para concatenar valores de várias linhas"
author: "bw3sley"
slug: "concatenate-grouped-values-with-string-agg"
tags:
  - mssql
  - strings
  - aggregates
created_at: "2022-08-03"

---

# Usar `STRING_AGG()` para concatenar valores de várias linhas

`STRING_AGG()` junta valores de várias linhas em uma única string com separador definido.

```sql
SELECT STRING_AGG(Name, ', ') AS NomesConcatenados
FROM Employees;
-- João, Maria, Pedro, Ana
```
