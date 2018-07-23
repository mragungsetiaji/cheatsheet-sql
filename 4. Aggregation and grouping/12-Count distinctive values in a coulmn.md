## Instruction
Great. As you probably expect, we can also add the keyword DISTINCT in our function count():

````sql
SELECT count(DISTINCT customer_id) FROM orders;
````

This time, we count all rows which have a distinctive value in the column customer_id. In other words, this instruction tells us how many different customers have placed an order so far. If a customer places 5 orders, the customer will only be counted once.

---
## Exercise
Count how many different positions there are in the table employees.

