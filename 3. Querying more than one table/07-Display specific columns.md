## Instruction
Splendid! Now, let's say we only **need a few columns** in our result. We just want to know the model of the car and the owner's name, Take a look:

> `SELECT person.name, car.model 
FROM person JOIN car 
ON person.id = car.owner_id;`
Simple, isn't it? Instead of the asterisk (`*`), we put the column names.

As we now have more than one table, we put the table name in front of the column name and we separate them with a dot (`.`). In this way, SQL knows that the column model belongs to the table car, etc.

---
## Exercise
Select director name and movie title from tables `movie` and `director` in such a way that a movie is shown together with its director.