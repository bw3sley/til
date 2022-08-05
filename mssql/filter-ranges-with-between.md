---
title: "Usar `BETWEEN` para filtrar intervalos"
author: "bw3sley"
slug: "filter-ranges-with-between"
tags:
  - mssql
  - tsql
  - filters
created_at: "2026-07-05"

---

# Usar `BETWEEN` para filtrar intervalos

`BETWEEN` inclui limites inicial e final ao filtrar números, datas ou texto.

```sql
SELECT *
FROM Products
WHERE Price BETWEEN 10 AND 20;
```
