# STUFF
The `STUFF()` function deletes a part of a string and then inserts another part into the string, starting at a specified position.

Tip: Also look at the `REPLACE()` function.

Eg:
```sql
    SELECT STUFF('SQL Tutorial', 1, 3, 'TypeScript'); -- TypeScript Tutorial 
```