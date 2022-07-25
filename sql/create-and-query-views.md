---
title: "Usar `VIEW` para salvar uma consulta reutilizável"
author: "bw3sley"
slug: "create-and-query-views"
tags:
  - sql
  - views
created_at: "2026-07-05"

---

# Usar `VIEW` para salvar uma consulta reutilizável

Uma `VIEW` encapsula um `SELECT` em um objeto consultável como se fosse tabela virtual.

```sql
CREATE VIEW Report AS
SELECT Customer.Name, Address.City
FROM Customer
LEFT JOIN Address ON Customer.Customer_Id = Address.FK_Customer_Id;
```
