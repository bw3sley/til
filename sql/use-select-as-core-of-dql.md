---
title: "Usar `SELECT` como comando central da DQL"
author: "bw3sley"
slug: "use-select-as-core-of-dql"
tags:
  - sql
  - dql
  - select
created_at: "2022-08-01"

---

# Usar `SELECT` como comando central da DQL

DQL é a parte do SQL voltada para consulta, e `SELECT` é o comando que combina projeção, origem e filtro na mesma leitura.

```sql
SELECT User.Name, User.Email
FROM User
WHERE User.Id = 1;
```

Esse padrão cobre o caso mais comum de consulta: escolher colunas, dizer de onde vêm e filtrar o resultado.
