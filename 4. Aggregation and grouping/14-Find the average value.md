## Instruction
OK, now that you know what best salary is, let's discuss another function:

````sql
SELECT avg(total_sum) FROM orders 
WHERE customer_id = 100;
````

The function avg() finds the average value of the specified column.

In our example, we'll get the average order value for the customer with id 100.

---
## Exercise
Find the average salary in the table employees for the year 2013.