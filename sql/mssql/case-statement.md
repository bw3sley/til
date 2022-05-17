# CASE

A declaração **CASE** percorre condições e retorna um valor quando a primeira condição é atendida (semelhante a um comando *if-then-else*). Assim que uma condição for verdadeira, o **CASE** interrompe a verificação e retorna o resultado. Se nenhuma condição for verdadeira, o valor definido na cláusula **ELSE** será retornado.

Se não houver uma cláusula **ELSE** e nenhuma condição for atendida, o resultado será `NULL`.

Exemplo:

```sql
SELECT
    CASE 
        WHEN Cars.Brand = 'FIAT' THEN 1
        WHEN Cars.Brand = 'CHEVROLET' THEN 2
        ELSE 'Não encontrado'
    END AS Informacao,
    
    * 
FROM Cars;
```

## Referências

- [📄 W3Schools — SQL CASE Statement](https://www.w3schools.com/sql/sql_case.asp)