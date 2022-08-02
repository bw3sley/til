---
title: "Usar `ISNUMERIC()` para testar se valor é numérico"
author: "bw3sley"
slug: "check-if-value-is-numeric-with-isnumeric"
tags:
  - mssql
  - tsql
  - validation
created_at: "2026-07-05"

---

# Usar `ISNUMERIC()` para testar se valor é numérico

`ISNUMERIC()` retorna `1` quando a expressão pode ser interpretada como número e `0` caso contrário.

```sql
SELECT ISNUMERIC('4567');
-- 1

SELECT ISNUMERIC('Olá Mundo');
-- 0
```
