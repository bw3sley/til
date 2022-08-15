---
title: "Usar `DELIMITER` ao criar procedure no MySQL"
author: "bw3sley"
slug: "create-stored-procedures-with-delimiter"
tags:
  - mysql
  - procedures
created_at: "2026-07-05"

---

# Usar `DELIMITER` ao criar procedure no MySQL

Ao definir procedure no MySQL, troque o delimitador temporariamente para poder usar `;` dentro do bloco `BEGIN ... END`.

```sql
DELIMITER //

CREATE PROCEDURE GetUserInfo(IN userId INT)
BEGIN
  SELECT * FROM users WHERE id = userId;
END //

DELIMITER ;
```
