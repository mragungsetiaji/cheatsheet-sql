## Instruction
We know who directed a specific movie because there is a column `director_id` in the table `movie`. If you take a look at "Midnight in Paris", its `director_id` is 3. So we can now look into directors to find out that id 3 is assigned to Woody Allen. And that's how we know he is the director. Did you get that right?

There are quite a few ways of getting information from multiple tables at the same time. We're going to start with the easiest one.

> `SELECT * FROM person, car;`

You already know how `SELECT * FROM` works, don't you? Now we just name two tables instead of one, and we separate them with a comma (`,`). Piece of cake! The result, however, might be a tiny bit of a surprise to you. Let's check that out.

----
## Exercise
Get all the data from two tables: `movie` and `director`.

If there are 8 movies and 5 directors, **how many rows will we get in our result?** Think about it before you press Run and check code