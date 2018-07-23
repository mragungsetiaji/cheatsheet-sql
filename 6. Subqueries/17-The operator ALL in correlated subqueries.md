## Instruction
Good. Still remember the operator ALL? Let's use it in a correlated subquery.

````SQL
SELECT * FROM trip main_trip 
WHERE price >= ALL (SELECT price FROM trip sub_trip 
   WHERE main_trip.city_id = sub_trip.city_id);
````

The above query looks for all trips which are the most expensive of all trips to that specific city. The instructions only choose trips with their price equal to or greater than all trip prices in the specific city.

---
## Exercise
Select the hiking trip with the longest distance (column length) for every mountain.