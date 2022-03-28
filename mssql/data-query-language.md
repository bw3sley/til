# DQL - Data Query Language
DQL statements are used for performing queries on the data within schema objects. The purpose of the DQL Command is to get some schema relation based on the query passed to it. We can define DQL as follows it is a component of SQL statement that allows getting data from the database and imposing order upon it

</br>

## SELECT
Like its name says, It's a command that selects something from database.

Eg:
```
    SELECT 
        Name, 
        Email,
        Gender -- (PROJECTION)
    
    FROM User - (ORIGIN)

    INNER JOIN Address // (JOIN)
        ON User.Id = Adreess.Id_User

    WHERE Id = 1 // (SELECTION)
```