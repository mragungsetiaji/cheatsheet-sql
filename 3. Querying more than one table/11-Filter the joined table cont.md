## Instruction
Excellent! Filtering the results is very important, so let's do another exercise on that. Do you still remember how text values work in SQL?

````sql
SELECT person.id, car.model 
FROM person JOIN car 
ON person.id = car.owner_id WHERE car.brand = 'Fiat';
````

In the above query, we only select cars branded `'Fiat'`. Piece of cake, right? Let's practice.

---
## Exercise
Select all columns from tables `movie` and `director` in such a way that a movie is shown together with its director. Select only those movies which were directed by Steven Spielberg.