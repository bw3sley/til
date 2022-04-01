# UNION
The **UNION** operator is used to combine the result-set of two or more **SELECT** statements.

- Every **SELECT** statement within **UNION** must have the same number of columns
- The columns must also have similar data types
- The columns in every **SELECT** statement must also be in the same order
- **UNION** selects only distinct values
- **UNION ALL** to also select duplicate values

Eg:
```
    SELECT 
        City, 
        Country 
        
    FROM Customers
    
    WHERE Country = 'Germany'
    
    UNION
    
    SELECT 
        City, 
        Country 
        
    FROM Suppliers
    
    WHERE Country = 'Germany'
    
    ORDER BY 
        City;
```