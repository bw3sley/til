---
title: "Usar `COMMIT`, `ROLLBACK` e `SAVE TRANSACTION` no SQL Server"
author: "bw3sley"
slug: "use-commit-rollback-and-save-transaction"
tags:
  - mssql
  - transactions
created_at: "2026-07-05"

---

# Usar `COMMIT`, `ROLLBACK` e `SAVE TRANSACTION` no SQL Server

No SQL Server, transações podem ser confirmadas com `COMMIT`, desfeitas com `ROLLBACK` e parcialmente revertidas com `SAVE TRANSACTION`.

```sql
BEGIN TRAN;
UPDATE Customer SET CustomerName = 'w3sLeYY' WHERE Customer.Id > 2;
ROLLBACK TRAN;
```
