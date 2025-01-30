---
title: "Escolher o tipo de `JOIN` pelo resultado esperado"
author: "bw3sley"
slug: "choose-the-right-join-for-each-result-shape"
tags:
  - sql
  - joins
created_at: "2022-07-25"

---

# Escolher o tipo de `JOIN` pelo resultado esperado

`INNER JOIN` retorna só correspondências. `LEFT`, `RIGHT` e `FULL` preservam lados diferentes quando não há match.

```sql
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
LEFT JOIN Orders ON Customers.CustomerID = Orders.CustomerID;
```
