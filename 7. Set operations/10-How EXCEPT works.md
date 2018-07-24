## Instruction
Good job. Amazing people, aren't they?

The next keyword is: EXCEPT. Let's change our example one more time:

````sql
SELECT person FROM cycling 
WHERE country = 'Germany'
EXCEPT
SELECT person FROM skating 
WHERE country = 'Germany';
````

So what does EXCEPT do? It shows all the results from the first (left) table with the exception of those that also appeared in the second (right) table.

In our example, we will see all people from Germany who won a medal in cycling MINUS the people from Germany who also won a medal in skating.

---
## Exercise
Find all the countries which have a medal in cycling but not in skating.