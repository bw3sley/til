---
title: "Entender modelos conceitual, lógico e físico na modelagem"
author: "bw3sley"
slug: "understand-conceptual-logical-and-physical-models"
tags:
  - sql
  - database-design
created_at: "2022-07-26"

---

# Entender modelos conceitual, lógico e físico na modelagem

Separar modelo conceitual, lógico e físico ajuda a não misturar regra de negócio com detalhe de implementação cedo demais.

O conceitual define o que existe, o lógico organiza relacionamentos e o físico transforma isso em tabela, coluna, índice e tipo no SGBD.

Exemplo: `Cliente` e `Pedido` podem existir no modelo conceitual antes de virar `VARCHAR(100)`, chave estrangeira ou índice.
