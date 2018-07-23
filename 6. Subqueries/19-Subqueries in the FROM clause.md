## Instruction
Good job! Now, queries can also be used in other places. We can, for example, use a subquery instead of a table in the FROM clause.

````SQL
SELECT * 
FROM city, (SELECT * 
   FROM country 
   where area < 1000) AS small_country 
    WHERE small_country.id = city.country_id;
````

The above query finds cities from small countries. Of course, there is no table small_country in our database, so... we create it 'on the fly' with a subquery in the FROM clause. Of course, we need a name for it, so we use an alias with the keyword AS. In the end, the query shows cities together with their countries provided that the country has an area below 1 000. Remember how selecting from two tables works? We need the condition in the WHERE clause, because otherwise each city would be shown together with every possible country.

---
## Exercise
Show mountains together with their countries. The countries must have at least 50 000 residents.