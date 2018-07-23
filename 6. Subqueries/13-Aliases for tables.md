## Instruction
Wow! It wasn't easy, so congratulations! Now, there may be examples where the same table is used in the main query as well as in the correlated subquery. Try to find out what the following example returns:

```SQL
SELECT * FROM city main_city 
WHERE population > (SELECT avg(population) 
 FROM city  average_city    
 WHERE average_city.country_id = main_city.country_id);
```

In this example, we want to find cities with the population greater than the average population in all cities of the specific country. The problem is that we look for cities in the main clause and check the average population value for cities in the subquery. The same table appears twice - no good.

This is why we must use aliases for tables. Take a look: in the subquery we put ... FROM city average_city ... and in the main query ... FROM city main_city. As you can see, we gave new temporary names for the table city, different for the main query and for the subquery. The temporary name (the so-called alias) is put after the table name, separated with a space. No commas here, remember!

----
## Exercise
Find all information about cities with the rating higher than the average rating for all cities in that specific country.