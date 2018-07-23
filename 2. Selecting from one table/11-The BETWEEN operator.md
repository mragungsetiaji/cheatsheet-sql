## Instruction
Good. Now, if you want to find users who are above 13 and below 70, you can of course use the previous example:

> `SELECT id, name 
FROM user 
WHERE age < 70 AND age > 13;`

But there is also another way of writing the example above. Take a look:

> `SELECT id, name 
FROM user 
WHERE age BETWEEN 13 AND 70;`

We introduced a new keyword `BETWEEN` which simply means that we look for rows with the age column set to be anything between 13 and 70, including these values.

Note, however, that some database systems can produce different results - in some of them, the values 13 and 70 are not included in the results. Always check how `BETWEEN` works in your database.

## Exercise
Select `vin`, `brand` and `model` of all cars which were produced between 1995 and 2005.