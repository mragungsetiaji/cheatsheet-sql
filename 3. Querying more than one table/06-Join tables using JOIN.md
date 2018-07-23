## Instruction
Take a look at the following example:

> `SELECT * FROM person JOIN car 
ON person.id = car.owner_id;`

We want to join the tables `person` and `car`, so we use the keyword `JOIN` between their names.

SQL should also know how to join the tables, so there is another keyword `ON`. After it, we set our condition: join only those rows where the `id` in `person` is the same as `owner_id` in car.

---
## Exercise
Use the new construction `JOIN ... ON` to join rows from the tables `movie` and `director` in such a way that a movie is shown together with its director.