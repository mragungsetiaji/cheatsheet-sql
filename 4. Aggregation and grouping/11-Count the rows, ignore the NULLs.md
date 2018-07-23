## Instruction
Naturally, the asterisk (`*`) isn't the only option available in the function `count()`. For example, we may ask the database to count the values in a specific column:

````sql
SELECT count(customer_id) FROM orders;
````

What's the difference between `count(*)` and `count(customer_id)`? Well, the first option counts all rows in the table and the second option counts all rows where the column `customer_id` has a specified value. In other words, if there is a `NULL` in the column `customer_id`, it won't be counted.

---
## Exercise
Check how many non-NULL values in the column `position` there are in the table `employees`.