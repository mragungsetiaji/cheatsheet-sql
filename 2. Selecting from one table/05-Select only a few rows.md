## Instruction
Our table is pretty small, so if we wanted to get some information about Volkswagens, we could select all rows and just ignore the extra few which contain other brands. **But what if our table consisted of thousands of rows?**

> `SELECT * FROM user WHERE id = 100;`

Look what happened. We've added `WHERE` and a **condition**. The simplest condition looks like the one in our example - we want to retrieve information about a user with a specific id (100), so we use the equality (`id = 100`).

## Exercise
Select all columns for those cars which were produced (column `production_year`) in 1999.