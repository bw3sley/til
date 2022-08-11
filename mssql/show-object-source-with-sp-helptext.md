---
title: "Usar `sp_helptext` para ver código-fonte de view ou procedure"
author: "bw3sley"
slug: "show-object-source-with-sp-helptext"
tags:
  - mssql
  - metadata
  - procedures
created_at: "2026-07-05"

---

# Usar `sp_helptext` para ver código-fonte de view ou procedure

`sp_helptext` exibe o script T-SQL de objetos como views, functions, triggers e stored procedures.

```sql
sp_helptext 'usp_GetCustomerDetails';
```
