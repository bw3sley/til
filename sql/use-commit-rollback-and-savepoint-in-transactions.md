---
title: "Usar `COMMIT`, `ROLLBACK` e `SAVEPOINT` em transações"
author: "bw3sley"
slug: "use-commit-rollback-and-savepoint-in-transactions"
tags:
  - sql
  - transactions
  - tcl
created_at: "2026-07-05"

---

# Usar `COMMIT`, `ROLLBACK` e `SAVEPOINT` em transações

Na TCL, `COMMIT` confirma alterações, `ROLLBACK` desfaz e `SAVEPOINT` cria ponto intermediário de retorno.

```sql
BEGIN TRANSACTION;
DELETE FROM Orders WHERE OrderDate < '2023-01-01';
ROLLBACK;
```
