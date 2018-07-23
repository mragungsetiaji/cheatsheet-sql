## Instruction
Awesome! Let's learn another new operator, then. Consider the following:

```SQL
SELECT * FROM city 
WHERE EXISTS (SELECT * FROM trip
     WHERE city_id = city.id);
```

EXISTS is a new operator. It checks if there are any rows that meet the condition.

In our case, the whole query will show only such cities where there is at least one trip (where there exists a trip) organized by our travel agency. Cities with no trips will not be shown.

## Exercise
Select all countries where there is at least one mountain.