---
title: "Usar `--` e `/* */` para comentar SQL"
author: "bw3sley"
slug: "write-single-line-and-multiline-comments"
tags:
  - sql
  - comments
created_at: "2026-07-05"

---

# Usar `--` e `/* */` para comentar SQL

`--` comenta uma linha. `/* ... */` comenta múltiplas linhas ou trechos embutidos.

```sql
-- comentário de linha única
SELECT * FROM /* tabela de clientes */ Customers;
```
