# DDL - Data Definition Language
DDL is a set of SQL commands used to create, modify, and delete database structures but not data. These commands are normally not used by a general user, who should be accessing the database via an application.

</br>

## CREATE
This command is used to create the database or its objects (like table, index, function, views, store procedure, and triggers).

Eg:
```sql
    CREATE DATABASE Store;

    CREATE TABLE Customers (
        Id BIGINT PRIMARY KEY IDENTITY,
        CustomerName VARCHAR(50),
        CustomerGender CHAR(1),
    );
```

</br>

## DROP
This command is used to delete objects from the database.

Eg:
```sql
    DROP DATABASE Store;

    DROP TABLE Customers;
```

</br>

## ALTER
This is used to alter the structure of the database.

### Adding columns

Eg:
```sql
    ALTER TABLE Student ADD (Age NUMERIC(5,2), Course VARCHAR(40));
```

### Modifying columns

Eg:
```sql
    ALTER TABLE Student MODIFY Course VARCHAR(20);
```

### Dropping columns 

Eg:
```sql
    ALTER TABLE Student DROP COLUMN Course;
```

You can find more about [clicking here]()

</br>

## TRUNCATE
This is used to remove all records from a table, including all spaces allocated for the records are removed.

- Truncate is normally ultra-fast and its ideal for deleting data from a temporary table.
- Truncate preserves the structure of the table for future use, unlike drop table where the table is deleted with its full structure.
- Table or Database deletion using DROP statement cannot be rolled back, so it must be used wisely.


Eg:
```sql
    TRUNCATE TABLE Customers;
```