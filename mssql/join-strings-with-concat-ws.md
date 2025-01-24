---
title: "Usar `CONCAT_WS()` para concatenar com separador"
author: "bw3sley"
slug: "join-strings-with-concat-ws"
tags:
  - mssql
  - strings
created_at: "2022-08-09"

---

# Usar `CONCAT_WS()` para concatenar com separador

`CONCAT_WS()` junta várias strings usando um separador fixo entre elas.

```sql
SELECT CONCAT_WS('.', 'www', 'W3Schools', 'com');
-- www.W3Schools.com
```
