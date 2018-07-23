## Instruction
Good. As you can see, the lowest salary was shown first and the highest salary last. This **ascending** order of results is performed in SQL by default. If you want to be precise and make things clear, however, you can use the keyword `ASC` (short for the ascending order) after the column name:

````sql
SELECT * FROM orders ORDER BY total_sum ASC;
````

Adding the keyword `ASC` will change nothing, but it will show your intensions in a very clear way.

We can also **reverse the order** and make the greatest values appear first.

````sql
SELECT * FROM orders ORDER BY total_sum DESC;
````

As you can see, we've added the word `DESC` after the column name, which is short for the **descending** order. As a result, the greatest values in the column `total_sum` will be shown first

---
## Exercise
Select all rows from the table `employees` and sort them in the **descending** order by the column `last_name`.