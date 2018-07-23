## Instruction
Could you see the problem? There were many rows with the same year, so each year is shown many times in the results.

In our orders example, if there were many orders placed by the same customer, each customer id would be shown many times in the results. **No good**.

Fortunately, we can easily change it.

````sql
SELECT DISTINCT customer_id FROM orders;
````

Before the column names, we've added the word `DISTINCT`. Now the database will **remove duplicates** and only show DISTINCT values. Each `customer_id` will appear only once.

---
## Exercise
Select the column `year` from the table `employees` in such a way that each year is only shown once.