# ACID

ACID é um acrônimo que representa quatro propriedades fundamentais para garantir a confiabilidade em transações de banco de dados: **Atomicidade**, **Consistência**, **Isolamento** e **Durabilidade**.

## Atomicidade

Garante que todas as operações de uma transação sejam concluídas com sucesso ou, em caso de falha, nenhuma alteração seja realizada no banco de dados. Ou seja, a transação é indivisível; se uma parte falha, toda a transação é revertida.

## Consistência

Assegura que uma transação leva o banco de dados de um estado consistente a outro estado consistente, respeitando todas as regras de integridade e restrições definidas, como tipos de dados e chaves primárias.

## Isolamento

Garante que transações simultâneas não interfiram umas nas outras. Cada transação ocorre de forma independente, evitando que operações concorrentes causem inconsistências nos dados.

## Durabilidade

Assegura que, uma vez confirmada (commit), uma transação terá seus efeitos permanentemente preservados no banco de dados, mesmo em casos de falhas ou reinicializações do sistema.

## Referências

- [📄 Databricks](https://www.databricks.com/br/glossary/acid-transactions)