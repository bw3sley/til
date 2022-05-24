# ISNUMERIC

A função `ISNUMERIC()` verifica se uma expressão é numérica.

Essa função retorna **1** se a expressão for numérica e **0** caso contrário.

Exemplo:

```sql
SELECT ISNUMERIC('4567'); -- Retorna 1
SELECT ISNUMERIC('Olá Mundo'); -- Retorna 0
```