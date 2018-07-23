## Instruction
Excellent. You can also use DISTINCT on a group of columns. Take a look:

````SQL
SELECT DISTINCT customer_id, order_date FROM orders;
````

One customer may place many orders every day, but if we just want to know on what days each customers actually did place at least one order, the above query will check that.

---
## Exercise
Check what positions there are in every department. In order to do that, select the columns department and position from the table employees and eliminate duplicates.