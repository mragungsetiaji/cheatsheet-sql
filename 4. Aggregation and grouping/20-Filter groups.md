## Instruction
In this section, we'll have a look at how groups can be filtered. There is a special keyword HAVING reserved for that.

````sql
SELECT customer_id, order_date, sum(total_sum) 
FROM orders 
GROUP BY customer_id, order_date 
HAVING sum(total_sum) > 2000;
````
The new part here comes at the end. We've put the keyword HAVING and then stated the condition to filter the results. In this case, we only want to show those customers who, on individuals days, ordered goods for the total daily value of more than 2 000.

By the way, this is probably a good moment to point out an important thing: in SQL, the specific fragments must be always put in the right order. You can't, for example, put WHERE before FROM. Similarly, HAVING must always follow GROUP BY, not the other way around. Keep that in mind when you write your queries, especially longer ones.

---
## Exercise
Find such employees who (have) spent more than 2 years in the company. Select their last name and first name together with the number of years worked.