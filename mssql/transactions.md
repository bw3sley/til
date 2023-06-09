# Transactions
Transactions group a set of tasks into a single execution unit. Each transaction begins with a specific task and ends when all the tasks in the group successfully complete. If any of the tasks fail, the transaction fails. Therefore, a transaction has only two results: success or failure.

</br>

## COMMIT
If everything is in order with all statements within a single transaction, all changes are recorded together in the database is called committed. The COMMIT command saves all the transactions to the database since the last COMMIT or ROLLBACK command.

Eg:
```sql
    BEGIN TRAN
        UPDATE Customer
            SET Customer.CustomerName = 'w3sLeYY'

    WHERE Customer.Id > 2

    COMMIT TRAN
```

</br>

## ROLLBACK
If any error occurs with any of the SQL grouped statements, all changes need to be aborted. The process of reversing changes is called rollback. This command can only be used to undo transactions since the last COMMIT or ROLLBACK command was issued. 

Eg:
```sql
    BEGIN TRAN
        UPDATE Customer
            SET Customer.CustomerName = 'w3sLeYY'

    WHERE Customer.Id > 2

    ROLLBACK TRAN
```

</br>

## SAVEPOINT
A SAVEPOINT is a point in a transaction in which you can roll the transaction back to a certain point without rolling back the entire transaction. 

Eg:
```sql
    SAVEPOINT SP1;

        DELETE FROM Student WHERE AGE = 20;

    SAVEPOINT SP2;

    ROLLBACK TO SP1;
```

This command is used only in the creation of SAVEPOINT among all the transactions. 
In general ROLLBACK is used to undo a group of transactions.

### RELEASE SAVEPOINT
This command is used to remove a SAVEPOINT that you have created. 

Eg:
```sql
    RELEASE SAVEPOINT SP2;
```

Once a SAVEPOINT has been released, you can no longer use the ROLLBACK command to undo transactions performed since the last SAVEPOINT.