#RDBMS

## What is Database normalization 
 - Normalization is a database deign technique that reduces data redundancy and eliminates undesirable characteristics like insertion, Update and Deletion Anomalies.
 - The purpose of Normalization in SQL is to eliminate redundant (repetitive) data and ensure data is stored logically.

## DB Normal Forms
1. NF(First Normal Form)
2. NF(Second Normal Form)
3. NF (Third Normal Form)
4. CNF (Boyce-Codd Normal Form) - Edger Codd and Raymond F. Boyce
5. NF( Fourth Normal Form)
6. NF (Fifth Normal Form)
7. NF (Sixth Normal Form)

## Understanding Normalization 
- Assume, a video library maintains a database of movies rented out. Without any normalization in database, all information is stored in one table as shown below.
- Here you see Movies Rented column has multiply values. 


### 1NF
#rules 

- Each table cell should contain a single value
- Each Record needs to be unique.

## Primary Key / Composite Key
- A primary key has following attributes:
	- A **Primary key** cannot be NULL
	- A primary key value must be unique 
	- The primary key values should rarely be changed
	- The primary key must be given a value when a new record is inserted.
	- Tew or more columns that

## Keys
- In our database we have two people with the same name Robert Phil, but they live in different places.
- Hence, we require both full name and address to identify

### 2NF
#rules 

- Rule 1 - Be in 1 NF
- Rule 2 - Single Column Primary Key that does not functionally dependent on any subset of candidate key relation.
- It is clear that we can't move forward to make a simple database in 2an Normalization form unless we partition the table above. 
## Transitive functional dependencies
- A Transitive **functional dependency** is when changing a non-key column, might cause any of the other non-key columns to change.
- Consider the table 1. Changing the non-key column Full name may change Salutation. 

### 3NF
- We have again divided our tables and creat