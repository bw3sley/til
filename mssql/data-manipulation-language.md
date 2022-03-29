# DML - Data Manipulation Language
The SQL commands that deals with the manipulation of data present in the database belong to **DML** or **Data Manipulation Language** and this includes most of the SQL statements. It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.

</br>

## INSERT
**INSERT** commands in SQL are used to insert data records or rows in a database table. In an **INSERT** statement, we specify both the column_names for which the entry has to be made along with the data value that has to be inserted.

Eg:
```
    INSERT INTO Customer (
        Customer_Name, 
        Customer_Gender, 
        Customer_Email
    ) 
            
    VALUES (
        'Wesley', 
        'M', 
        'w3sley@example.com'
    );
```

</br>

## UPDATE
**UPDATE** command or statement is used to modify the value of an existing column in a database table.

Eg:
```
    UPDATE Cliente 
        SET Email = ‘example@example.com’ 
        
    WHERE Id_Cliente = 1;
```

### UPDATE more than one value

Eg:
```
    UPDATE Customer 
        SET Customer_Gender = 'M' 
        
    WHERE Customer_Id IN (1, 2, 3, 4)
```

### UPDATE using JOIN

Eg:
```
    UPDATE Users 
        SET Biography = 'Abobrinha'
    
    FROM User
	
    INNER JOIN Biography
	    ON Users.Id = Biography.FK_Id_User
    
    WHERE User.Id = 3
```

</br>

## DELETE
**DELETE** statement in SQL is used to remove one or more rows from the database table. It does not delete the data records permanently. We can always perform a rollback operation to undo a **DELETE** command. With **DELETE** statements we can use the **WHERE** clause for filtering specific rows.

Eg:
```
    DELETE FROM Customer
    WHERE Customer_Id = 1
```

### DELETE more than one value

Eg:
```
    DELETE FROM Customer
    WHERE Customer_Id IN (1, 2, 3, 4)
```

### DELETE using JOIN

Eg:
```
    DELETE 
        Users
    
    FROM User
	
    INNER JOIN Biography
	    ON Users.Id = Biography.FK_Id_User

    WHERE Users.Id = 3
```