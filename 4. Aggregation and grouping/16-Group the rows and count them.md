## Instruction
In the previous section, we've learnt how to count statistics for all rows. We'll now go on to study even more sophisticated statistics. Look at the following statement:

````sql
SELECT customer_id, count(*) from orders 
GROUP BY customer_id;
````

The new piece here is GROUP BY followed by a column name (customer_id). GROUP BY will group together all rows having the same value in the specified column.

In our example, all orders made by the same customer will be grouped together in one row. The function count(*) will then count all rows for the specific clients. As a result, we'll get a table where each customer_id will be shown together with the number of orders placed by that customer.

Take a look at the following table which illustrates the query:

|order_id|customer_id|order_date|ship_date|total_sum|customer_id|count(*)|
|---|---|---|---|---|---|---|
|1|	1|	21-02-2014|	22-02-2014|	1009.00|	1|	3|
|2|	1|	25-02-2014|	25-02-2014|	2100.00|||	 	 
|3|	1|	03-03-2014|	03-03-2014|	315.00|||	 	 
|4|	2|	03-03-2014|	04-03-2014|	401.67|	2|	2|
|5|	2|	03-03-2014|	07-03-2014|	329.29|||	 	 
|6|	3|	15-03-2014|	15-03-2014|	25349.68|	3|	1|
|7|	4|	19-03-2014|	20-03-2014|	2324.32|	4|	4|
|8|	4|	02-04-2014|	02-04-2014|	7542.21|||	 	 
|9|	4|	05-04-2014|	07-04-2014|	123.23|||	 	 
|10|	4|	05-04-2014|	07-04-2014|	425.33|||	 	 
|11|	5|	06-04-2014|	09-04-2014|	2134.65|	5|	5|
|12|	5|	17-04-2014|	19-04-2014|	23.21|||	 	 
|13|	5|	25-04-2014|	26-04-2014|	5423.23|||	 	 
|14|	5|	29-04-2014|	30-04-2014|	4422.11|||	 	 
|15|	5|	30-04-2014|	30-04-2014|	532.54|||	 	

---
## Exercise
Find the number of employees in each department in the year 2013. Show the department name together with the number of employees.

