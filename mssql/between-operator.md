# BETWEEN
The **BETWEEN** operator selects values within a given range. The values can be numbers, text, or dates.

Eg:
```sql
    SELECT 
        * 
    
    FROM Products
    
    WHERE Price BETWEEN 10 AND 20;
```

## NOT BETWEEN
To display the products outside the range of the previous example, use ``NOT BETWEEN``.

Eg:
```sql
    SELECT 
        * 
        
    FROM Products
    
    WHERE Price NOT BETWEEN 10 AND 20;
```

## BETWEEN Text values
It selects all products with a ProductName between Carnarvon Tigers and Mozzarella di Giovanni.

Eg:
```sql
    SELECT 
        * 
    
    FROM Products
    
    WHERE ProductName BETWEEN 'Carnarvon Tigers' 
        AND 'Mozzarella di Giovanni'
    
    ORDER BY ProductName;
```