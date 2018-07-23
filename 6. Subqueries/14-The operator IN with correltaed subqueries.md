## Instruction
Wow, cool! Now, remember the operator IN? It allowed us to specify a few values in the WHERE clause, so it worked a bit like the OR operator. Now, take a look:

```SQL
SELECT * FROM city 
WHERE country_id IN (SELECT id FROM country 
   WHERE id = city.country_id 
AND country.population < 40000);
```

Can you predict what the above instruction does? It shows all cities from such countries where the total population of the country is less than 40 000.

## Exercise
Show all information about all trips to cities with their rating lower than 4.