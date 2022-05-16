# BETWEEN

O operador **BETWEEN** seleciona valores dentro de um intervalo definido. Os valores podem ser números, textos ou datas.

Exemplo:

```sql
SELECT 
    * 
FROM Products
WHERE Price BETWEEN 10 AND 20;
```

## NOT BETWEEN

Para exibir os produtos fora do intervalo do exemplo anterior, use o operador `NOT BETWEEN`.

Exemplo:

```sql
SELECT 
    * 
FROM Products
WHERE Price NOT BETWEEN 10 AND 20;
```

## BETWEEN com valores de texto

É possível usar o operador **BETWEEN** para filtrar valores de texto. O exemplo abaixo seleciona todos os produtos com `ProductName` entre *Carnarvon Tigers* e *Mozzarella di Giovanni*.

Exemplo:

```sql
SELECT 
    * 
FROM Products
WHERE ProductName BETWEEN 'Carnarvon Tigers' 
    AND 'Mozzarella di Giovanni'
ORDER BY ProductName;
```

## Referências

- [📄 W3Schools — SQL BETWEEN Operator](https://www.w3schools.com/sql/sql_between.asp)