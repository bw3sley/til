---
title: "Usar `mysqldump` para exportar banco em arquivo"
author: "bw3sley"
slug: "dump-database-with-mysqldump"
tags:
  - mysql
  - backup
  - cli
created_at: "2026-07-05"

---

# Usar `mysqldump` para exportar banco em arquivo

`mysqldump` gera um snapshot do banco em SQL e normalmente é redirecionado para arquivo.

```bash
mysqldump my_database > my_database_backup.sql
```
