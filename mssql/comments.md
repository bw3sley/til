# Comments
As is any programming languages comments matter a lot in SQL also. In this set we will learn about writing comments in any SQL snippet

</br>

## Single line comments
Comments starting and ending in a single line are considered as single line comments. Line starting with ``-`` is a comment and will not be executed.

Eg:
```
    -- single line comment
    -- another comment
```

## Multi line comments
Comments starting in one line and ending in different line are considered as multi line comments. Line starting with ``/*`` is considered as starting point of comment and are terminated when ``*/`` is encountered.

Eg:
```
    /* multi line comment
    another comment */
```
 
## In line comments 
In line comments are an extension of multi line comments, comments can be stated in between the statements and are enclosed in between ``/*`` and ``*/``.

Eg:
```sql
    SELECT * FROM /* Customers; */ 
    SELECT * FROM -- Customers
```