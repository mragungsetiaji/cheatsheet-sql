## Instruction
Very good! We'll now focus on another aspect. By default, the database returns every row which matches the given criteria. This is what we normally expect, of course, but there are cases when we might want to change this behavior.

Imagine the following situation: we want to get the ids of all customers who have ever placed an order. We might use the following code:

````sql
SELECT customer_id FROM orders;
````
What's wrong with the code in this case? Well, try to do the exercise to find out.

---
## Exercise
Select the column `year` for all rows in the table employees. Then examine the result carefully.