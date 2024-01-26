# Part 1 - Algebra Queries:
Write relational algebra expressions that will produce a relation containing:
• Q1: Loan number with loan amount less than $20000.
- Πloan_number(σloan_amount<20000(Loan))

• Q2: Customers’ name and email, city, and mobile number with their branch names.
- Πname,email,city,mobile_number(Costumers ⋈ branch_id = id Branch)

• Q3: Retrieve the total amount of transactions per each account.
- Πaccount_number, total_amount​(σaccount_number, total_amount (Account⋈account_number = acc_number​Transaction))

• Q4: Retrieve all the customers having their account in “active” state and balance more
than $10000.
- σstate=′active′∧balance>10000​(Customer⋈account_number = acc_number​Account)
# Part 2 - SQL Queries:
Write a SQL command for the following:
• Q1: Retrieve the customers who are not living in “Gjøvik” (Returns 9 records)

- ``SELECT * FROM `customer` WHERE customer.City <> 'Gjøvik' 

• Q2: Retrieve the customers who have their email address under the Norwegian internet
domain (.no) (Returns 9 records)

- ``SELECT * FROM `customer` WHERE customer.Email LIKE '%.no'

• Q3: Retrieve the information of loans given to the customers in each branch who have
loan period 3 years. (Returns 8 records)

- 

• Q4: Retrieve the customers who have not taken any loan. (Returns 2 record)

• Q5: Write a SQL query that retrieves top 3 youngest customers who have taken loans.
(Returns 3 records)

• Q6: Retrieve the number of transactions and sum of amount for each account during the
year 2020 (Returns 10 records)

• Q7: Add a new customer with information below then open an inactive account in the
given branch:
o Name: Ryan Ishus
o Address
o City : Trondheim
o Street: Bakkegata
o No: 15
o Postal_code: 7049
o Home_Phone : 75432103
o Mobile_phone: 45464783
o Email : ryan00@realmail.no
o Customer_id: 10016
o Gender: Male
o Birth_date: 1991-01-10
o Branch: b2
o Account_number=ac1001
o Balance=$1000
o Opening_date= 2021-01-18
o Status= Inactive

• Q8: Update the “Status” of account of customer Ryan Ishus to “Active”.

• Q9: Delete the loans that have a loan period of N