# Views
In SQL, a view is a virtual table based on the result-set of an SQL statement.

A view contains rows and columns, just like a real table. The fields in a view are fields from one or more real tables in the database.

You can add SQL statements and functions to a view and present the data as if the data were coming from one single table.

- You can't **INSERT** or **DELETE** a View that contains a **JOIN**. You only can **UPDATE**.
- You can **INSERT**, **DELETE** or **UPDATE** a View that doesn't contain **JOIN**.

## Creating a View

Eg:
```
    CREATE VIEW Report AS
	    SELECT 
			Customer.Name,
			Customer.Gender,
			Customer.Email,

			Address.City,
			Addres.UF

        FROM Customer

        LEFT JOIN Address
            ON Customer.Customer_Id = Address.FK_Customer_Id
	
	    WHERE Customer.Email IS NOT NULL
```

## Selecting a View

Eg:
```
    SELECT * FROM Report
```

## Deleting a View

Eg:
```
    DROP VIEW Report
```