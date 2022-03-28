# Normalization 
Normalization is a database design technique that reduces data redundancy and eliminates undesirable characteristics like Insertion, Update and Deletion Anomalies. Normalization rules divides larger tables into smaller tables and links them using relationships. The purpose of Normalisation in SQL is to eliminate redundant (repetitive) data and ensure data is stored logically.

</br>

## First Normal Form
- Each table cell should contain a single value.
- Each record needs to be unique.

</br>

## Second Normal Form
- Be in 1NF.
- Single Column Primary Key that does not functionally dependant on any subset of candidate key relation.

</br>

## Third Normal Form
- Be in 2NF
- Has no transitive functional dependencies

</br>

There are more rules that I won't be covering on this post, but feel free to check this [What's Normalization in DBMS](https://www.guru99.com/database-normalization.html)