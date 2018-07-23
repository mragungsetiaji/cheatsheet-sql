## Instruction
Awesome! Subqueries can also be used within the column list in a SELECT clause. Here, it's important that the subquery returns exactly one row and column.

Take a look:

````SQL
SELECT name, 
(SELECT count(*) FROM trip WHERE city_id = city.id) AS trip_count 
FROM city;
````
In the above query, we provide the name of each city together with the number of trips to that city. Notice that we use the function count() to count the number of trips for each city.

---
## Exercise
Show each mountain name together with the number of hiking trips to that mountain (name the column count).

