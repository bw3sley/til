---
title: "Usar `sp_columns` para ver metadados de colunas"
author: "bw3sley"
slug: "inspect-column-metadata-with-sp-columns"
tags:
  - mssql
  - metadata
created_at: "2022-08-08"

---

# Usar `sp_columns` para ver metadados de colunas

`sp_columns` retorna detalhes como nome, tipo, tamanho e nulabilidade das colunas de um objeto.

É útil quando você precisa confirmar definição de coluna direto no banco, sem abrir a tabela visualmente.

```sql
sp_columns Customer;
```
