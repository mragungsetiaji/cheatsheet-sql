## Instruction
Correct! There's one more thing before you go. Groups can be sorted just like rows. Take a look:

````sql
SELECT customer_id, order_date, sum(total_sum) 
FROM orders 
GROUP BY customer_id, order_date 
ORDER BY sum(total_sum) DESC;
````
In this case, we'll order our rows according to the total daily sum of all orders by a specific customer. The rows with the highest value will appear first.

---
## Exercise
Sort the employees according to their summary salaries in the company. Greatest values should appear first. Show the last name, the first name and the sum.

