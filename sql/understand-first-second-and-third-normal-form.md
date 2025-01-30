---
title: "Entender 1FN, 2FN e 3FN na normalização"
author: "bw3sley"
slug: "understand-first-second-and-third-normal-form"
tags:
  - sql
  - normalization
created_at: "2022-07-27"

---

# Entender 1FN, 2FN e 3FN na normalização

As três primeiras formas normais ajudam a reduzir repetição e evitar anomalias de inserção, atualização e exclusão.

Na prática: 1FN evita múltiplos valores na mesma célula, 2FN remove dependências parciais e 3FN remove dependências transitivas.

Exemplo: em vez de repetir endereço em várias linhas do cliente, extraia esse dado para uma tabela relacionada.
