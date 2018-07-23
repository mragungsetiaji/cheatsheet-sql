## Instruction
Excellent! Of course, count(*) isn't the only option. In fact, GROUP BY is used together with many other functions. Take a look:

````sql
SELECT customer_id, max(total_sum) 
FROM orders 
GROUP BY customer_id;
````

We've replaced count(*) with max(total_sum). Can you guess what happens now?

That's right, instead of counting all the orders for specific clients, we'll find the order with the highest value for each customer.

---
## Exercise
Show all departments together with their lowest and highest salary in 2014.

