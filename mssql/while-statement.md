# WHILE
SQL WHILE loop provides us with the advantage to execute the SQL statement(s) repeatedly until the specified condition result turn out to be false.

Eg:
```
    DECLARE Counter INT = 0
	
    BEGIN
		WHILE (Counter <= 10)
			
            BEGIN
				PRINT 'Counter value = ' + CAST(@Counter AS VARCHAR) 
				SET @Counter = @Counter + 1			
			END
    END
    GO
```