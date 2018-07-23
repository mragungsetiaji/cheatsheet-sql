## Instruction
Good. To sum up this section, let's find out about one more operator: ANY. Take a look:

````SQL
SELECT * FROM trip 
WHERE price < ANY (SELECT price 
FROM hiking_trip 
WHERE mountain_id = 1);
````

In the above example, we want to find trips to the cities which are cheaper than any hiking trip to the mountain with id 1 (Mont Blanc, just to let you know). There are two hiking trips to Mont Blanc: one which costs 1000 and one which costs 300. If we find a city trip which is cheaper than any of these values, we show it in the result.

Again, other logical operators are possible: = ANY, =! ANY, < ANY, <= ANY, >= ANY.

---
## Exercise
Find all information about all the city trips which have the same price as any hiking trip.