# ROW_NUMBER
The ROW_NUMBER() is a window function that assigns a sequential integer to each row within the partition of a result set. The row number starts with 1 for the first row in each partition.

Eg:
```sql
    SELECT 
        ROW_NUMBER() OVER ( ORDER BY CustomerName ) AS ID,
        Customer.*
    
    FROM Customer
```