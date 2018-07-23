## Instruction
Up until now, we were able to filter the rows in the previous examples using conditional operators (`=`, `!=`, `<`, `>`, `<=`, `>=`). But what about situations when we want to be really picky and join a few conditions?

> `SELECT id, name 
FROM user 
WHERE age > 50 OR height < 185;`

We've added a new OR clause which allows us to join more conditions.

In this case, we only select those users who are above 50 years of age or under 185 cm of height. In other words, a row is displayed when the first condition or the second condition is true. Note that if both conditions are true, the row is also displayed.

## Exercise
Select vin of all cars which were produced before 2005 or whose price is below 10 000.