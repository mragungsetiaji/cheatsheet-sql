## Instruction
Great! Now, what happens if we don't know precisely what we're looking for? With text values, you can always use the `LIKE` operator instead of the equality sign. What change does it make? Well, take a look at the following example:

> `SELECT * FROM user WHERE name LIKE 'A%';`

`LIKE` allows for the use of the percentage sign (`%`). The percentage sign (`%`) applied in the **example replaces any number (zero or more) of unknown characters.**

As a result, we'll obtain all users whose name begins with the letter 'A'. We may not remember someone's exact name, but we know it begins with an A and it's enough. Convenient, isn't it?

---
## Exercise
Select `vin`, `brand` and `model` of all cars whose brand begins with an F.