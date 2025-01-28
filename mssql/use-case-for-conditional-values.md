---
title: "Usar `CASE` para retornar valores condicionais"
author: "bw3sley"
slug: "use-case-for-conditional-values"
tags:
  - mssql
  - tsql
  - case
created_at: "2022-08-12"

---

# Usar `CASE` para retornar valores condicionais

`CASE` avalia condições em ordem e retorna o valor da primeira que for verdadeira.

```sql
SELECT CASE
  WHEN Cars.Brand = 'FIAT' THEN 1
  WHEN Cars.Brand = 'CHEVROLET' THEN 2
  ELSE 'Não encontrado'
END AS Informacao
FROM Cars;
```
