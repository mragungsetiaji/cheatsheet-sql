## Instruction
Let's start off with a new keyword UNION. What is a union? Well, to cut a long story short, it combines results of two or more queries. Let's analyze the example:

````sql
SELECT * FROM cycling 
WHERE country = 'Germany'
UNION
SELECT * FROM skating 
WHERE country = 'Germany';
````

As you can see, we first selected all medals for Germany from the table cycling, then we used the keyword UNION and finally we selected all medals for Germany from the table skating.

You may be tempted to ask: could we split this instruction into two separate queries? Of course we could. But using a UNION, we get all results for the first table PLUS the results of the second table shown together. Remember to only put the semicolon (;) at the very end of the whole instruction!

---
## Exercise
Show all the medals for the period between 2010 and 2014 for skating and cycling. Use the UNION keyword.

