## Instruction
Okay! Now, you probably wonder how to use the new operator IN with subqueries. Consider the following example:

````sql
SELECT price FROM trip 
WHERE city_id IN 
   (SELECT city_id 
FROM city 
WHERE population < 2000000);
````

In the subquery, we look for ids of all cities with their population below 2 million. Next, we use these ids as the values in the IN operator.

In this way, we can find prices of trips to cities with their population lower than 2 million.

---
## Exercise
Find all information about all trips in cities with their area over 100.