## Instruction
We can join even more conditions using **brackets**, according to our needs. If we want to find only those users who are above 70 years old or below 13 AND who are at least 180 cm tall, we can use the following expression:

> `SELECT id, name 
FROM user 
WHERE (age > 70 OR age < 13) AND (height >= 180);`

---
## Exercise
Select `vin` of all cars which were produced before 1999 or after 2005 and whose price is lower than 4 000 or greater than 10 000.