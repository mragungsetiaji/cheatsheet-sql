## Instruction
Good, let's get down to work.

You're already pretty skilled when it comes to filtering rows - but have you wondered how they are sorted in the result of an SQL query? Well, the answer is simple - by default, they are not sorted at all. The sequence in which rows appear is arbitrary and every database can behave differently. You can even perform the same SQL instruction a few times and get a different order each time - unless you ask the database to sort the rows, of course.

````sql
SELECT * FROM orders ORDER BY customer_id;
````

In the above example, we've added a new piece: `ORDER BY`. After this expression, you can simply specify a column on which the data will be sorted.

In this case, we give the column name `customer_id`, so all orders will be sorted in relation to customer_ids.

---
## Exercise
Try it yourself. Select all columns from the table employees and sort them according to the salary.