## Instruction
Amazing job! Now that we know how to work with columns, let's find out how to filter the results even further:

````sql
SELECT person.id, car.model 
FROM person JOIN car 
ON person.id = car.owner_id WHERE person.age < 25;
````

The new part here is the WHERE clause. Now we only look for such connections of cars and their owners where the owner is below 25. Be sure to include the table name in the condition (`person.age`).

---
## Exercise
Select all columns from tables `movie` and `director` in such a way that a movie is shown together with its director. Select only those movies which were made after 2000.