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

- Each table cell should contain a singel value
- 