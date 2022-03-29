# LIKE
The **LIKE** command is used in a **WHERE** clause to search for a specified pattern in a column.

You can use two wildcards with LIKE:

- ``%`` - Represents zero, one, or multiple characters
- ``_`` - Represents a single character (MS Access uses a question mark (?) instead)

</br>

## "%" Wildcard

### Starts with
It selects everything that starts with ``something%``.

Eg:
```
    SELECT 
        * 
        
    FROM Customer 
    
    WHERE Customer_Name LIKE 'w3sLeYY%'
```

### Ends with
It selects everything that finishes with ``%something``.

Eg:
```
    SELECT 
        * 
    
    FROM Customer 
    
    WHERE Customer_Name LIKE '%w3sLeYY'
```

### Contains 
It selects everything that contains ``%something%``.

 Eg:
```
    SELECT 
        * 
        
    FROM Customer 
    
    WHERE Customer_Name LIKE '%w3sLeYY%'
```

### Starts with and ends with
It selects everything that starts and finishes with ``s%g``.

Eg:
```
    SELECT 
        * 
        
    FROM Customer 
    
    WHERE Customer_Name LIKE 'w%y'
```

</br>

## "_" Wildcard

### Length
It  selects everything that starts with "a" and are at least 3 characters in length.

Eg:
```
    SELECT 
        * 
        
    FROM Customers
    
    WHERE Customer_Name LIKE 'a__%';
```