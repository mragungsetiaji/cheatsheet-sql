## Instruction
Keep up the good work! There is one more logical operator worth mentioning: `NOT`. Basically speaking, whatever is stated after `NOT` will be negated:

> `SELECT * 
FROM user 
WHERE age NOT BETWEEN 20 AND 30;`

In the above example we placed `NOT` in front of a `BETWEEN` clause. As a result, we'll get all users except for those aged 20 to 30.

---
## Exercise
Select `vin`, `brand` and `model` of all cars except for those produced between 1995 and 2005.