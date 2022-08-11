---
title: "Usar `STUFF()` para remover e inserir trecho em uma string"
author: "bw3sley"
slug: "replace-part-of-string-with-stuff"
tags:
  - mssql
  - strings
created_at: "2026-07-05"

---

# Usar `STUFF()` para remover e inserir trecho em uma string

`STUFF()` apaga parte de uma string a partir de uma posição e insere outro texto no lugar.

```sql
SELECT STUFF('SQL Tutorial', 1, 3, 'TypeScript');
-- TypeScript Tutorial
```
