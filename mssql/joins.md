# JOINS
A **JOIN** clause is used to combine rows from two or more tables, based on a related column between them.

</br>

## Different Types of JOINS

### INNER JOIN
Returns records that have matching values in both tables.

Eg:
```
    SELECT 
        Orders.OrderID, 
        Customers.CustomerName

    FROM Orders

    INNER JOIN Customers 
        ON Orders.CustomerID = Customers.CustomerID;
```

The **INNER JOIN** keyword selects all rows from both tables as long as there is a match between the columns. If there are records in the "Orders" table that do not have matches in "Customers", these orders will not be shown!

### LEFT JOIN
Returns all records from the left table, and the matched records from the right table.

Eg:
```
    SELECT 
        Customers.CustomerName, 
        Orders.OrderID
    
    FROM Customers
    
    LEFT JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
    
    ORDER BY 
        Customers.CustomerName;
```

The **LEFT JOIN** keyword returns all records from the left table (table1), and the matching records from the right table (table2). The result is 0 records from the right side, if there is no match.

### RIGHT JOIN
Returns all records from the right table, and the matched records from the left table.

Eg:
```
    SELECT 
        Orders.OrderID, 
        Employees.LastName, 
        Employees.FirstName
    
    FROM Orders
    
    RIGHT JOIN Employees 
        ON Orders.EmployeeID = Employees.EmployeeID
    
    ORDER BY 
        Orders.OrderID;
```

The RIGHT JOIN keyword returns all records from the right table (table2), and the matching records from the left table (table1). The result is 0 records from the left side, if there is no match.

### FULL OUTTER JOIN
Returns all records when there is a match in either left or right table.

Eg:
```
    SELECT 
        Customers.CustomerName, 
        Orders.OrderID
    
    FROM Customers
    
    FULL OUTER JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
    
    ORDER BY 
        Customers.CustomerName;
```

The **FULL OUTER JOIN** keyword returns all records when there is a match in left (table1) or right (table2) table records.

### SELF JOIN
A self join is a regular join, but the table is joined with itself.

Eg:
```
    SELECT 
        CustomerA.CustomerName AS CustomerNameA, 
        CustomerB.CustomerName AS CustomerNameB, 
        CustomerA.City
    
    FROM Customers CustomerA, Customers CustomerB
    
    WHERE CustomerA.CustomerID <> CustomerNameB.CustomerID
        AND CustomerA.City = CustomerNameB.City
    
    ORDER BY 
        CustomerA.City;
```