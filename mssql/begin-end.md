# BEGIN...END
The **BEGIN...END** statement is used to define a statement block. A statement block consists of a set of SQL statements that execute together. A statement block is also known as a batch.

In other words, if statements are sentences, the **BEGIN...END** statement allows you to define paragraphs.

Eg:
```sql
    BEGIN
        SELECT
            Products.Id,
            Products.Name

        FROM Products
        
        WHERE
            Products.Price > 100000;

        IF @@ROWCOUNT = 0
            PRINT 'No product with price greater than 100000 found';
    END
```