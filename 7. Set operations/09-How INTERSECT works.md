## Instruction
Excellent. Here is another keyword: INTERSECT. Let's change our example a little bit:

````sql
SELECT year FROM cycling 
WHERE country = 'Germany' 
INTERSECT 
SELECT year FROM skating 
WHERE country = 'Germany';
````

Instead of UNION (or UNION ALL), we've put INTERSECT in there. What's the difference?

Well, UNION gave you all the results from the first query PLUS the results from the second query. INTERSECT, on the other hand, only shows the rows which belong to BOTH tables.

In this case, we would get the years when Germany got a medal in cycling AND speed skating at the same time.

The conditions here stay the same: the number of columns in both tables must be the same and the number or text values must match.

----
## Exercise
Find names of each person who has medals both in cycling and in skating.

