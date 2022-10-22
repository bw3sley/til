# ISNUMERIC
The `ISNUMERIC()` function tests whether an expression is numeric.

This function returns 1 if the expression is numeric, otherwise it returns 0.

Eg:
```sql
    SELECT ISNUMERIC("4567"); -- Prints out 1
    SELECT ISNUMERIC("Hello World"); -- Prints out 0
```