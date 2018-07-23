## Instruction
Alright, to give you an idea of what subqueries are, analyze the following problem: we want to find cities which have the same rating as Paris.

With the knowledge you have now, you would first need to check the rating for Paris:

```sql
SELECT rating FROM city WHERE NAME = 'Paris';
```

Then you would need to write down the result of the above query somewhere in your notebook (the rating is 5, by the way) and then construct a new query:

```sql
SELECT name FROM city WHERE rating = 5;
```

Subqueries have been introduced to help you with such examples. They are 'queries inside queries' and they are always put in parentheses. Take a look:

```sql
SELECT name FROM city 
WHERE rating = (SELECT rating 
FROM city 
WHERE name = 'Paris');
```

The database will first check the subquery (in the parentheses), then write the results of the query (in this case, number 5) instead of the subquery and then check the final query.

In this particular example, you must write the subquery in such a way that it returns precisely one value (one column of one row) so that it matches the equation 'rating = X'. It wouldn't make much sense to put a whole table there, would it?

## Exercise
Show all information about all cities which have the same area as Paris.