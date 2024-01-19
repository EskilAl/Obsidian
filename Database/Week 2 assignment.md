Q1:
• What is the result of: Πname(county)?
	- it get's the county column names. 

Q2:
• What is the result of: Πid, city(dealer)?
	- it fetches the column id and city in table dealer.

Q3:
• What is the result of: Πid, make, model, year(car)?
	- it fetches the column id , make, model, year in table car 

Q4:
• What relational algebra expression defines a relation containing names of dealer cities in the
dealer relation?
	- Πcity(dealer) 

Q5:
• What relation algebra expression defines a relation containing the id, make, type, year,
mileage, and price of cars in the car relation?
	-Πid, make, type, year, mileage, price(car)

Q6:
• What is the result of: σyear < 2010 OR mileage > 50000(car)?
	- select a car that is older than 2010 or has a higher milage than 50000 in table car("entire object").

Q7:
• What is the result of: σfuel <> 'diesel'(car)?
	- select all fuel that is not equal to diesel in car and receives the entire object in the table. 

Q8:
• What is the result of: σmake IN ('Mercedes-Benz', 'Audi')(car)?
	- get's the entire object of a car in the table car with the name of Mercedes-Benz and Audi 

Q9:
• What relational algebra expression defines a relation containing rows from the car relation
where the car is either a station wagon or costs no more than 360,000?

Q10:
• What relational algebra expression defines a relation containing rows from the car relation
where the car is not an Audi or a Volkswagen

Q11:
• Decompose this expression: Πcity(σcounty_no = 34(dealer))?
• What is the result?

Q12:
• Decompose this expression: σdealer_id IN ('Gjvk', 'Hmr', 'Lhr')(Πid, make, year, dealer_id(car))?
• What is the result?

Q13:
• What relational algebra expression defines a relation containing the ids from the dealer
relation where the dealer resides in the county with county number 18 or county number
50?

Q14:
• What relational algebra expression defines a relation containing the id, make, model, type,
and price from the car relation where the car is either a station wagon or a suv and the
price is between 300,000 and 450,000?
Q15:
• What relational algebra expression defines a relation containing id, make, model, and type
from the car relation where the car is not an SUV?
Q16:
• What is the result of:
Πcity, make, model(σfuel <> 'diesel'(car ⨝dealer_id = dealer.id
dealer))?
Q17:
• Which of these expressions are equivalent – if any:
o car  dealer
o σdealer_id = dealer.id(car  dealer)
o car ⨝dealer_id = dealer.id
dealer
Q18:
• What relational algebra expression defines a relation containing county name and city
names for dealers in the counties named Trøndelag or Nordland:
Q19:
• What relational algebra expression defines a relation containing city name, maker name for
cars on sale in the county named Innlandet?
Q20:
• What relational algebra expression defines a relation containing county name, make, and
year for cars of type suv costing less than 400,000?
Q21:
• What relational algebra expression defines a relation containing city name, make, year, and
price for hybrid or diesel cars on sales by dealers in the cities of Gjøvik, Hamar or
Lillehammer:
Q22:
• What is the result of: Πcity, make, model(car ⟖dealer_id = dealer.id
dealer)?
Q22:
• Which of these expressions are equivalent – if any:
o car ⨝dealer_id = dealer.id
dealer
o car ⟕dealer_id = dealer.id
dealer
o car ⟖dealer_id = dealer.id
dealer
Q23:
• What relational algebra expression defines a relation containing the city name and the make
name for 2019 and 2020 cars on sale in all the cities – even those that have no such cars for
sale.
Q24
• What is the result of: COUNT id(σfuel = 'petrol'(car))
Q25
• What is the result of:
MIN mileage, MAX mileage(car ⨝dealer_id = dealer.id dealer
⨝county_no = no σname = 'Innlandet'(county))
Q26
• What is the result of:
COUNT dealer.id(σcar.id IS NULL(car ⟖dealer_id = dealer.id
dealer))
Q27:
• What relational algebra expression defines a relation that holds the year of the oldest car for
sale.
Q28:
• What relational algebra expression defines a relation counting the number of Volkswagen
Passat cars for sale in the cities of Harstad and Bardufoss combined.
Q29
• What is the result of:
city SUM price(car ⨝dealer_id = dealer.id dealer)
Q30
• What is the result of:
city, make SUM price(car ⨝dealer_id = dealer.id dealer)
Q30
• What is the result of:
σSUM price > 750000(city, make SUM price(car ⨝dealer_id = dealer.id dealer))
Q31:
• What relational algebra expression defines a relation that holds the average mileage per
year for cars for sale.
Q32:
• What relational algebra expression defines that holds the number of cars per type per
county.