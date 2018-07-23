## Instruction
Great! Remember, `NULL` is a special value. You can't use the equals sign to check whether something is `NULL`. **It simply won't work**. The opposite of `IS NOT NULL` is `IS NULL`.

> `SELECT id 
FROM user 
WHERE middle_name IS NULL;`

This query will return only those users who don't have a middle name, i.e. their `middle_name` is unknown.

---
## Exercise
Select all cars whose price column is a `NULL` value.