## Instruction
In every row, there can be `NULL` values, i.e. fields with unknown missing values. Remember the Opel from our table with its missing price? This is exactly a `NULL` value. We simply don't know the price.

To check whether a column has a value, we use a special instruction `IS NOT NULL`.

> `SELECT id 
FROM user 
WHERE middle_name IS NOT NULL;`

This code selects only those users who have a middle name, i.e. their column `middle_name` is known.

---
## Exercise
Select all cars whose price column isn't a null value.