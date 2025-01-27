---
title: "Usar `sp_help` para inspecionar detalhes de um objeto"
author: "bw3sley"
slug: "inspect-object-details-with-sp-help"
tags:
  - mssql
  - metadata
created_at: "2022-08-09"

---

# Usar `sp_help` para inspecionar detalhes de um objeto

`sp_help` mostra informações gerais de tabela, view ou procedure, incluindo estrutura e índices.

É útil para inspecionar um objeto rapidamente no SQL Server sem navegar manualmente por catálogo, designer ou metadados separados.

```sql
sp_help Customer;
```
