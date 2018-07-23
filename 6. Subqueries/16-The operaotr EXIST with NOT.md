## Instruction
Good! Remember the operator NOT? We can use it together with EXISTS. Take a look:

````SQL
SELECT * FROM city 
WHERE NOT EXISTS (SELECT * FROM trip 
    WHERE city_id = city.id);
````

As you probably predict, this query will find all cities that don't have a trip organized to them.

---
## Exercise
Select all mountains with no hiking trips to them.