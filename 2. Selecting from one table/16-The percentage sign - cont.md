## Instruction
That's the way to go! Of course, the percentage sign (`%`) can be put anywhere between the single quotes and as many times as it's necessary:

> `SELECT * FROM user WHERE name LIKE '%A%';`

That's right, the example above will select any user **whose name contains at least one 'A'.**

Remember that the percentage sign (`%`) can also replace zero characters, so the name can also begin and end with the A.

---
## Exercise
Select vin of all cars whose model ends with an s.