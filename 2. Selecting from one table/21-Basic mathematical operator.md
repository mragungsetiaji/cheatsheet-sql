## Instruction
Nice! We may now move on to our next problem: **simple mathematics**. Can you add or multiply numbers in SQL? Yes, you can! Take a look at the example:

> `SELECT * 
FROM user 
WHERE (monthly_salary * 12) > 50000;`

In the above example, we multiply the monthly salary by 12 to get the annual salary by using the asterisk (`*`). We may then do whatever we want with the new value - in this case, we compare it with 50 000.

In this way, you can add (`+`), subtract (`-`), multiply (`*`) and divide (`/`) numbers.

## Exercise
Select all cars with the tax value over 2000. The tax value for all cars is 20% and you can write it as 0.20 in your query. Multiply the price by 0.20 to get the tax value.