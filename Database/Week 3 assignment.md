# In-class exercises

Week 2024-03

## SQL exercises

Given these sample tables:

![[Pasted image 20240124092211.png]]

Q1:

- What is a SQL equivalent to:   σmodel_year < 2010 OR mileage > 50000(car)?
	- `SELECT * FROM car WHERE model_year > 2010 OR mileage > 50000` 

Q2:

·         What is a SQL equivalent to:  Πid, make, model, type, price(σtype IN ('station wagon', 'suv')  
                                 AND price BETWEEN 300000 AND 450000(car))
- `SELECT id, make, model,type,price FROM car WHERE type IN ('station wagon' , 'suv') AND price BETWEEN 300000 AND 450000` 

Q3:

·         What is a SQL equivalent to:  Πcity, make, model(σfuel <> 'diesel'(car  ⨝dealer_id = dealer.id dealer))?
- ``SELECT city, make, model FROM (car INNER JOIN dealer ON dealer_id = dealer.id) WHERE fuel <> 'diesel'

Q4:

·         What is the relational algebra expression equivalent to:  
SELECT id, make, model, model_year, comment  
FROM car  
WHERE comment IS NOT NULL

- Πid,make,model,model_year,comment(σcomment IS NOT NULL(car))  

Q5:

·         Write a SQL statement that will return the name of the county, the city of the dealer, the id, model_year, mileage, and comment for Volkswagen Passats where the mileage is no more than 45000. Order the result on name of county, city of dealer, model_year (descending), and mileage (descending).

- 

Q6:

·       Write a SQL statement that will return the dealer city, id, make, model, age, and average mileage per year of cars for sale in the cities of Gjøvik, Hamar, and Lillehammer. The column showing the age of the car should be named age, the column showing the average mileage should be named yearly_mileage.

Q7:

·         Write a SQL statement that returns all information about cars having been used for demo purposes (i.e., the comment includes demo – case insensitive).

Q8:

·         Write a SQL statement that returns dealer city, make, model, and model_year for cars newer than 2015. Duplicates should be removed.

Q9:

·         What is a SQL equivalent to:  
Πcity, make, model(car  ⟖dealer_id = dealer.id dealer)?

Q10:

·         What is the relational algebra expression equivalent to:  
SELECT city, car.id, make    
FROM dealer LEFT OUTER JOIN car ON dealer_id = dealer.id  
WHERE city IN ('Jessheim', 'Elverum', 'Kongsvinger', 'Otta')  
  

Q11:

·         Write a SQL statement that returns county name, city name, model year for cars for sale. Duplicates should be removed. All dealers should be listed, even when there are no cars for sale at the dealer.

Q12:

·         What is a SQL equivalent to: MIN mileage, MAX mileage(car ⨝dealer_id = dealer.id dealer                ⨝county_no = no σname = 'Innlandet'(county))

Q13:

Write a SQL statement that returns the number of dealers that have Volkswagen cars for sale.

Q14:

·         What is a SQL equivalent to:  
city, make SUM price(car ⨝dealer_id = dealer.id dealer)

Q15:

·         What is a SQL equivalent to:  
σSUM price > 750000(city, make SUM price(car ⨝dealer_id = dealer.id dealer))

  

Q16:

·         What is the relational algebra expression equivalent to:  
SELECT fuel, AVG(price)  
FROM car  
GROUP BY fuel

Q17:

·         Write a SQL statement that returns the number of cars for each combination of make and fuel. Order the results on number of cars in descending order, then make and fuel in alphabetic order.

Q18:

·         Write a SQL statement that returns the number of cars of each make for sale in each county, but only for makes for which there are more than two cars for sale in that county.

Q19:

·         What is a SQL equivalent to:  
Πcity, make(dealer ⟕dealer_id = dealer.id σmodel_year IN (2019, 2020)(car)

Q20:

·         Write a SQL statement that lists the counties that don't have Volkswagen Passat cars.

Q21:

·         Write a SQL statement that lists the number of dealers per county, but only for the counties having more than average number of dealers among them.