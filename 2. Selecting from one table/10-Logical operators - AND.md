## Instruction
Excellent! Of course, `OR` isn't the only logical operator out there. Take a look at the next example:

>`SELECT id, name 
FROM user 
WHERE age < 70 AND age > 13;`

`AND` is another logical operator.

In this case, only those users will be selected whose age is above 13 **and** below 70. In other words, both conditions must be fulfilled to retrieve a particular row.

## Exercise
Select `vin` of all cars which were produced after 1999 and are cheaper than 7 000.