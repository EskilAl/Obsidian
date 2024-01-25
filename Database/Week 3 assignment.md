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

- `SELECT name,city, car.id, model_year, mileage, comment FROM (car INNER JOIN dealer ON dealer_id = dealer.id INNER JOIN county ON county_no = county.no) WHERE make ='volkswagen' AND model = 'Passat' AND mileage <= 45000 ORDER BY name,city,model_year DESC, mileage DESC`

Q6:

·       Write a SQL statement that will return the dealer city, id, make, model, age, and average mileage per year of cars for sale in the cities of Gjøvik, Hamar, and Lillehammer. The column showing the age of the car should be named age, the column showing the average mileage should be named yearly_mileage.
- ``SELECT dealer.city, dealer.id, car.id, car.model, 2024-car.model_year AS Age, (car.mileage/(2024-car.model_year)) AS yearly_mileage FROM (car INNER JOIN dealer ON dealer_id = dealer.id) WHERE dealer.city IN('Gjøvik','Hamar', 'Lillehammer')

Q7:

·         Write a SQL statement that returns all information about cars having been used for demo purposes (i.e., the comment includes demo – case insensitive).
- ``SELECT * FROM `car` WHERE comment LIKE 'Demo%'

Q8:

·         Write a SQL statement that returns dealer city, make, model, and model_year for cars newer than 2015. Duplicates should be removed.
- ``SELECT DISTINCT dealer.city, car.make, car.model, car.model_year  FROM (car INNER JOIN dealer ON dealer_id = dealer.id) WHERE car.model_year > 2015


Q9:

·         What is a SQL equivalent to:  
Πcity, make, model(car  ⟖dealer_id = dealer.id dealer)?
``SELECT dealer.city, car.make, car.model FROM (car RIGHT OUTER JOIN dealer ON dealer_id = dealer.id)

Q10:

·         What is the relational algebra expression equivalent to:  
SELECT city, car.id, make    
FROM dealer LEFT OUTER JOIN car ON dealer_id = dealer.id  
WHERE city IN ('Jessheim', 'Elverum', 'Kongsvinger', 'Otta')  

- Πcity, car.id, model(σ(city IN('Jessheim', 'Elverum', 'Kongsvinger', 'Otta')dealer ⟕ car_id = car.id car) 

Q11:

·         Write a SQL statement that returns county name, city name, model year for cars for sale. Duplicates should be removed. All dealers should be listed, even when there are no cars for sale at the dealer.

- ``SELECT DISTINCT county.name, dealer.city, car.model_year FROM (car Right OUTER JOIN dealer ON dealer_id = dealer.id RIGHT OUTER JOIN county ON county_no = county.no) WHERE 1

Q12:

·         What is a SQL equivalent to: MIN mileage, MAX mileage(car ⨝dealer_id = dealer.id dealer                ⨝county_no = no σname = 'Innlandet'(county))

- SELECT MIN(car.mileage) AS less, MAX(car.mileage) AS large FROM (car INNER JOIN dealer ON dealer_id = dealer.id INNER JOIN county ON county_no = county.no) WHERE county.name = 'Innlanded'

Q13:

Write a SQL statement that returns the number of dealers that have Volkswagen cars for sale.

- SELECT COUNT(car.id) AS Numbers_of_Volkswagen FROM (car INNER JOIN dealer ON dealer_id = dealer.id) WHERE make = 'Volkswagen'

Q14:

·         What is a SQL equivalent to:  
city, make SUM price(car ⨝dealer_id = dealer.id dealer)

- ``SELECT dealer.city, car.make, SUM(car.price) AS Total_Price FROM (car INNER JOIN dealer ON dealer_id = dealer.id) GROUP BY dealer.city, car.make

Q15:

·         What is a SQL equivalent to:  
σSUM price > 750000(city, make SUM price(car ⨝dealer_id = dealer.id dealer))

- ``SELECT dealer.city, car.make, SUM(car.price) AS Total_Price FROM(car INNER JOIN dealer ON dealer_id = dealer.id) GROUP BY dealer.city, car.make HAVING SUM(car.price) > 75000



Q16:

·         What is the relational algebra expression equivalent to:  
SELECT fuel, AVG(price)  
FROM car  
GROUP BY fuel

``Πfuel AVG(price)(car) 

Q17:

·         Write a SQL statement that returns the number of cars for each combination of make and fuel. Order the results on number of cars in descending order, then make and fuel in alphabetic order.

- ``SELECT car.make, car.fuel, COUNT(make) as combs FROM car GROUP BY make, fuel ORDER BY combs DESC ,make, fuel

Q18:

·         Write a SQL statement that returns the number of cars of each make for sale in each county, but only for makes for which there are more than two cars for sale in that county.

- ``SELECT car.make, COUNT(car.make) AS numbers_of_cars, county.name FROM (car INNER JOIN dealer ON dealer_id = dealer.id INNER JOIN county ON county_no = county.no) GROUP BY car.make, county.name HAVING COUNT(car.make) > 2

Q19:

·         What is a SQL equivalent to:  
Πcity, make(dealer ⟕dealer_id = dealer.id σmodel_year IN (2019, 2020)(car)

 - ``SELECT dealer.city, car.make, car.model_year IN (2019,2020) AS model_year FROM (car LEFT OUTER JOIN dealer ON dealer_id = dealer.id) WHERE car.model_year IN(2019,2020)

Q20:

·         Write a SQL statement that lists the counties that don't have Volkswagen Passat cars.

	-SELECT county.name,car.make, car.model FROM (car INNER JOIN dealer ON dealer_id = dealer.id INNER JOIN county ON county_no = county.no) WHERE car.model NOT IN ('Volkswagen', 'Passat') GROUP BY county.name,car.make

Q21:

·         Write a SQL statement that lists the number of dealers per county, but only for the counties having more than average number of dealers among them.

- ``