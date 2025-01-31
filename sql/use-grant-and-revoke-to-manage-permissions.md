---
title: "Usar `GRANT` e `REVOKE` para controlar permissões"
author: "bw3sley"
slug: "use-grant-and-revoke-to-manage-permissions"
tags:
  - sql
  - permissions
  - dcl
created_at: "2022-07-29"

---

# Usar `GRANT` e `REVOKE` para controlar permissões

Na DCL, `GRANT` concede acesso e `REVOKE` remove privilégios sobre tabelas, views ou procedures.

```sql
GRANT SELECT, INSERT ON Customers TO UserName;
REVOKE INSERT ON Customers FROM UserName;
```
