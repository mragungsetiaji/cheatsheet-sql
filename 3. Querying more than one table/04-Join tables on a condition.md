## Instruction
Surprised, huh? If there are 8 movies and 5 directors, most people will say that we'll get 5, 8 or 13 rows in the result. This is not true.

We've got 40 rows altogether because SQL takes every single movie and joins it with every possible director. So we now have 8 * 5 = 40 rows!

Why did it happen? SQL doesn't know what to do with the results from the two tables, so it gave you every possible connection. How can we change it? Take a look:

> `SELECT * FROM person, car 
WHERE person.id = car.owner_id;`

We've set a new condition in the `WHERE` clause. We now see only those connections where `id` from `person` is the same as `owner_id` from `car`. Makes sense, right?

Take a closer look at how we provide the information about columns in the `WHERE` condition. If you have multiple tables, you should refer to specific columns by giving the name of the table and the column, separated by a dot (`.`). As a result, the column `owner_id` from the table `car` becomes `car.owner_id` and so on.

---
## Exercise
Select all columns from tables `movie` and `director` in such a way that a movie is shown together with its director.