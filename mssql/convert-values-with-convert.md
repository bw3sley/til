---
title: "Usar `CONVERT()` para trocar tipo ou formato de valor"
author: "bw3sley"
slug: "convert-values-with-convert"
tags:
  - mssql
  - tsql
  - convert
created_at: "2022-08-04"

---

# Usar `CONVERT()` para trocar tipo ou formato de valor

`CONVERT()` muda o tipo de um valor e, em datas, também aceita estilos de formatação.

Diferença para `CAST()`: os dois convertem tipos, mas `CONVERT()` aceita um terceiro argumento com estilo de saída, muito usado para datas no SQL Server. `CAST()` é mais portátil entre bancos, mas não cobre esses formatos específicos.

```sql
SELECT CONVERT(varchar, Information.Date, 110)
FROM Information;
```
