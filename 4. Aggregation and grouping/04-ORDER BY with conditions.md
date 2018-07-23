## Instruction
Excellent! Now you can easily examine who's got the lowest and the highest salary. It's not that hard, as you can see.

We can filter rows and sort them at the same time. Just have a look:

````sql
SELECT * FROM orders 
WHERE customer_id = 100 
ORDER BY total_sum;
````

The `WHERE` clause and `ORDER BY` work well together.

In this case, we'll only see the orders made by the customer with id 100. The orders will be sorted on the total sum - the cheapest order will appear as the first result and the most expensive as the last one.

---
## Exercise
Select only the rows related to the year 2011 from the table `employees`. Sort them by salary.