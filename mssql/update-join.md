# UPDATE USING JOIN
To query data from related tables, you often use the join clauses, either inner join or left join. In SQL Server, you can use these join clauses in the UPDATE statement to perform a cross-table update.

Eg:
```
    UPDATE Users 
        SET Biography = 'Abobrinha'
    
    FROM User
	
    INNER JOIN Biography
	    ON Users.Id = Biography.FK_Id_User
    
    WHERE User.Id = 3
```