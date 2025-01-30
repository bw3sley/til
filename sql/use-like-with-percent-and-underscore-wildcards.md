---
title: "Usar `LIKE` com `%` e `_` para buscar padrões"
author: "bw3sley"
slug: "use-like-with-percent-and-underscore-wildcards"
tags:
  - sql
  - like
created_at: "2022-08-01"

---

# Usar `LIKE` com `%` e `_` para buscar padrões

`%` representa zero ou mais caracteres. `_` representa um caractere único.

```sql
SELECT *
FROM Customer
WHERE Customer_Name LIKE '%w3sLeYY%';
```
