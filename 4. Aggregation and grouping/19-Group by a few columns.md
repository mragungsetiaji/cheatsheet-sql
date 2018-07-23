## Instruction
Nice work.

There's one more thing about GROUP BY that we want to discuss. Sometimes we want to group the rows by more than one column. Let's imagine we have a few customers who place tons of orders every day, so we would like to know the daily sum of their orders.

````sql
SELECT customer_id, order_date, sum(total_sum) 
FROM orders 
GROUP BY customer_id, order_date;
````

As you can see, we group by two columns: customer_id and order_date. We select these columns alongside with the function sum(total_sum).

Remember: in such queries each column in the SELECT part must either be used later for grouping or it must be used with one of the functions.

It makes no sense to select any other column. For example, each order on the very same day by the very same customer can have a different shipping date. If you wanted to select the column ship_date in this case, the database wouldn't know which shipping date to choose for the whole group, so it would put just one, random value in the result.

To better understand the issue, take a look the following table:

|order_id|customer_id|order_date|ship_date|total_sum|(grouping)|customer_id|order_date|sum(total_sum)|ship_date|
|---|---|---|---|---|---|---|---|---|---|
|16|6|28-03-2015|29-03-2015|230.54|-->|6|28-03-2015|0|??|29-03-2015? 30-03-2015?|
|17|6|28-03-2015|30-03-2015|321.42|	-->||||||	 	 	 	 
|18|6|28-03-2015|30-03-2015|2354.23|	-->||||||		 	 	 	 
|19|6|29-03-2015|30-03-2015|4224.21|-->|6|29-03-2015|0|??|
|20|6|29-03-2015|30-03-2015|2314.32|	-->||||||		 	 	 	 
|21|6|29-03-2015|31-03-2015|124.21|	-->||||||		 	 	 	 
|22|6|29-03-2015|31-02-2015|4125.32|	-->||||||		 	 	 	 
|23|6|30-03-2015|03-04-2015|645.23|	-->|6|30-03-2015|0|??|
|24|6|30-03-2015|05-04-2015|7543.56|	-->||||||		 	 	 	 
|25|6|30-03-2015|05-04-2015|2315.63|	-->||||||		 	 	 	 
|26|7|02-04-2015|05-04-2015|523.98|	-->|7|02-04-2015|0|??|
|27|7|02-04-2015|06-04-2015|523.13|	-->||||||		 	 	 	 
|28|7|02-04-2015|07-04-2015|8533.31|	-->||||||		 	 	 	 
|29|7|03-04-2015|07-04-2015|4245.64|-->|7|03-04-2015|0|??|

---
## Exercise
Find the average salary for each employee. Show the last name, the first name and the average salary. Group the table by the last name and the first name.

