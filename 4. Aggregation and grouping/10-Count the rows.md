## Instruction
You already know that your database can do computation because we've already added or subtracted values in our SQL instructions. The database can do much more than that. It can compute statistics for multiple rows. This operation is called **aggregation**.

Let's start with something simple:

````sql
SELECT count(*) FROM orders;
````

Instead of the asterisk (`*`) which basically means 'all', we've put the expression `count(*)`. `Count(*)` is a function. A function in SQL always has a name followed by parentheses. In the parentheses, you can put information which the function needs to work. For example, `count()` calculates the **number of rows** specified in the brackets.

In this case, we've used `count(*)` which basically means 'count all rows'. As a result, we'll just get the number of all rows in the table orders - and not their content.

---
## Exercise
Count all rows in the table `employees`.