## Instruction
Good job. Alright, one more thing before we move on: you can sort your results by **more than one column** and each of them can be sorted in a **different** order:

````sql
SELECT * FROM order 
ORDER BY customer_id ASC, total_sum DESC;
````

As you can see, the results will be first sorted by `customer_id` in the ascending order (lowest values first) and then, for each customer_id, the orders will be sorted by the `total_sum` in the descending order (greatest values first).

---
## Exercise
Select all rows from the table `employees` and sort them in the **ascending** order by the **department** and then in the **descending** order by the **salary**.