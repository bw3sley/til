---
title: "Usar `FORMAT()` para aplicar máscara em valores"
author: "bw3sley"
slug: "format-values-with-format"
tags:
  - mssql
  - format
created_at: "2026-07-05"

---

# Usar `FORMAT()` para aplicar máscara em valores

`FORMAT()` permite exibir números ou datas com um padrão específico.

```sql
SELECT FORMAT(123456789, '##-##-#####');
-- 12-34-56789
```
