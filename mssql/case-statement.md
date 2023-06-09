# CASE
The **CASE** statement goes through conditions and returns a value when the first condition is met (like an if-then-else statement). So, once a condition is true, it will stop reading and return the result. If no conditions are true, it returns the value in the **ELSE** clause.

If there is no **ELSE** part and no conditions are true, it returns NULL.

Eg:
```sql
    SELECT
        CASE 
            WHEN Cars.Brand = 'FIAT' THEN 1
            WHEN Cars.Brand = 'CHEVROLET' THEN 2
        ELSE 'Not found'
        END Information,

    * FROM Cars
```