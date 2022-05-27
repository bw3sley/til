# ROW_NUMBER

A função **ROW_NUMBER()** é uma função de janela que atribui um número sequencial a cada linha dentro de uma partição do conjunto de resultados. A numeração começa em **1** para a primeira linha em cada partição.

Exemplo:

```sql
SELECT 
    ROW_NUMBER() OVER (ORDER BY CustomerName) AS ID,
    Customer.*
FROM Customer;
```

Neste exemplo, a função **ROW_NUMBER()** atribui um número sequencial a cada cliente, ordenando pelo nome.

---

## Referências

- [📄 W3Schools — SQL ROW_NUMBER() Function](https://www.w3schools.com/sql/func_sqlserver_row_number.asp)