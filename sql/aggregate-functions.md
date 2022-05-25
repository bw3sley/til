# Funções de Agregação

Uma função de agregação realiza um cálculo em um ou mais valores e retorna um único resultado. As funções de agregação são frequentemente usadas em conjunto com as cláusulas `GROUP BY` e `HAVING` em instruções `SELECT`.

</br>

## AVG

A função de agregação `AVG()` calcula a média dos valores não nulos em um conjunto.

Exemplo:

```sql
SELECT AVG(January) AS MediaVendasJaneiro FROM Sellers;
```

## COUNT

A função de agregação `COUNT()` retorna o número de linhas em um grupo, incluindo linhas com valores `NULL`.

Exemplo:

```sql
SELECT 
    Customer.Gender, 
    COUNT(*) AS TotalClientes
FROM Customer 
GROUP BY 
    Customer.Gender;
```

## MAX

A função de agregação `MAX()` retorna o maior valor (máximo) em um conjunto de valores não nulos.

Exemplo:

```sql
SELECT 
    MAX(January) AS MaiorVendaJaneiro 
FROM Sellers;
```

## MIN

A função de agregação `MIN()` retorna o menor valor (mínimo) em um conjunto de valores não nulos.

Exemplo:

```sql
SELECT 
    MIN(January) AS MenorVendaJaneiro 
FROM Sellers;
```

## SUM

A função de agregação `SUM()` retorna a soma de todos os valores não nulos em um conjunto.

Exemplo:

```sql
SELECT 
    Sellers.Seller_Gender, 
    SUM(January) AS TotalVendasJaneiro 
FROM Sellers
GROUP BY 
    Sellers.Seller_Gender;
```

## Referências

- [📄 W3Schools — SQL Aggregate Functions](https://www.w3schools.com/sql/sql_count_avg_sum.asp)