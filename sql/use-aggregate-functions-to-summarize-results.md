---
title: "Usar funções de agregação para resumir resultados"
author: "bw3sley"
slug: "use-aggregate-functions-to-summarize-results"
tags:
  - sql
  - aggregates
created_at: "2026-07-05"

---

# Usar funções de agregação para resumir resultados

Funções como `AVG()`, `COUNT()`, `MAX()`, `MIN()` e `SUM()` transformam várias linhas em um valor resumido.

```sql
SELECT COUNT(*) AS total_clientes FROM Customer;
-- Retorna quantidade total de clientes.
```
