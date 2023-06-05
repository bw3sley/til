# ACID
These are properties of a database transaction, and it is an acronym where Atomicity, Consistency, Isolation, and Durability.

## Atomicity
This property ensures that all transactions are atomic (indivisible), meaning that transactions are executed in their entirety. If an error occurs, all operations that make up the transaction will be rolled back.

## Consistency
The execution of a transaction must take the database from one consistent state to another consistent state, meaning that every transaction must adhere to the rules of data integrity (data type, primary key, constraints, etc.).

## Isolation
It does not allow multiple users to perform transactions on the same table, thus preventing one from interfering with the other.

## Durability
The effects of a transaction are permanent, and they can only be undone as a result of a subsequent and successful transaction.