## Instruction
Good. By default, UNION removes duplicate rows. Luckily, we can change it. Just put UNION ALL instead of UNION in your query

````sql
SELECT * FROM cycling 
WHERE country = 'Germany' 
UNION ALL 
SELECT * FROM skating 
WHERE country = 'Germany';
````
... and you'll get all rows, even when they are the same.

## Exercise
Show all countries which have medals in cycling or skating. Use a union. Don't remove duplicates.

