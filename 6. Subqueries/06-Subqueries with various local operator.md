## Instruction
Excellent! Subqueries can also be used with other logical operators. Take a look at the following example:

```sql
SELECT * FROM mountain 
WHERE height > (SELECT height 
FROM mountain 
WHERE name = 'Zugspitze');
```

The above query will return all mountains which are higher than Zugspitze. As you can see, we've used the 'greater than' sign (>) together with a subquery.

## Exercise
Find the names of all cities have a population lower than Madrid.