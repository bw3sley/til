---
title: "Entender as propriedades ACID de uma transação"
author: "bw3sley"
slug: "understand-acid-properties"
tags:
  - sql
  - transactions
  - acid
created_at: "2022-07-26"

---

# Entender as propriedades ACID de uma transação

ACID resume as garantias que evitam transações quebradas: atomicidade, consistência, isolamento e durabilidade.

Na prática, isso evita estado parcial. Em uma transferência, o débito e o crédito devem acontecer juntos ou a operação inteira precisa ser desfeita.

Exemplo: se o saldo sair da conta A, mas falhar antes de entrar na conta B, a transação deve dar `ROLLBACK`.
