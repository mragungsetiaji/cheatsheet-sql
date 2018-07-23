## Instruction
Great! Of course, you can pick just a few columns in such queries. Study the following example:

````SQL
SELECT name, days, price 
FROM trip, 
(SELECT * FROM city WHERE rating = 5) AS nice_city 
WHERE nice_city.id = trip.city_id;
````

The above query finds trips and their respective cities for such cities which are rated 5. It then shows the columns name, days, price for these tables. If the tables have all columns with different names, then you may drop the table names (i.e. you can write price instead of trip.price because there is just one column price anyway).

---
## Exercise
Show hiking trips together with their mountains. The mountains must be at least 3000 high. Select only the columns length and height.