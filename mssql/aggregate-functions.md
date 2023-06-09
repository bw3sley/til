# Aggregate functions
An aggregate function performs a calculation one or more values and returns a single value. The aggregate function is often used with the GROUP BY clause and HAVING clause of the SELECT statement.

</br>

## AVG
The ``AVG()`` aggregate function calculates the average of non-NULL values in a set.

Eg:
```sql
    SELECT AVG(January) AS AvgSellFromJanuary FROM Sellers
```

## COUNT
The ``COUNT()`` aggregate function returns the number of rows in a group, including rows with NULL values.

Eg:
```sql
    SELECT 
        Customer.Gender, 
        COUNT(*) 
        
    FROM Customer 
    
    GROUP BY 
        Customer.Gender;
```

## MAX
The ``MAX()`` aggregate function returns the highest value (maximum) in a set of non-NULL values.

Eg:
```sql
    SELECT 
        MAX(January) AS MaxSellFromJanuary 
    
    FROM Sellers
```

## MIN
The ``MIN()`` aggregate function returns the lowest value (minimum) in a set of non-NULL values.

Eg:
```sql
    SELECT 
        MIN(January) AS MinSellFromJanuary 
        
    FROM Sellers
```

## SUM
The ``SUM()`` aggregate function returns the summation of all non-NULL values a set.

Eg:
```sql
    SELECT 
        Sellers.Seller_Gender, 
        SUM(January) AS TotalSellsFromJanuary 
        
    FROM Sellers
    
    GROUP BY 
        Sellers.Seller_Gender
```