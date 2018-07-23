## Instruction
Nice! Next thing, our subqueries can become more complicated if we include some functions in them. Take a look:

````sql
SELECT * FROM hiking_trip 
WHERE length < (SELECT avg(length) FROM hiking_trip);
````

Now our query looks for all hiking trips with the distance shorter than the average. As you can see, we used the function avg() in the subquery which, as you might remember, gives us the average value from a column.

---
## Exercise
Find all information about trips whose price is higher than average.