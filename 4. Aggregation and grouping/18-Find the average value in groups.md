## Instruction
That's right!

Let's study one more example of this kind:

````sql
SELECT customer_id, avg(total_sum) 
FROM orders 
GROUP BY customer_id;
````

As you can see, we now have the function avg(total_sum) which will count the average order value for each of our customers.

---
## Exercise
Find the average salary in each department in 2015.