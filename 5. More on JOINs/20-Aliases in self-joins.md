## Instruction
That's right! Aliases are also convenient in other situations. Let's analyze the following situation:

We want to put information about children and their mothers into a database. At some point, we would also like to show children together with their mothers using a join.

Let's say we store both children and mothers in the same table person which has a column mother_id. This column contains the id of the person who is the mother and this id is taken from the very same table person.

The question is: can we join the table person with the table person? The answer is simple: yes, we can! You can't write

person join person
in your SQL query, but you can provide two different aliases for the same table:

 
````sql
SELECT * 
FROM person AS p1 
JOIN person AS p2 
ON p1.id = p2.mother_id;
````

Thanks to the aliases, the database engine will use the same table person twice - the first time to look for children and the second time to look for their mothers.

---
## Exercise
We want to know who lives with the student Jack Pearson in the same room. Use self-joining to show all the columns for the student Jack Pearson together with all the columns for each student living with him in the same room.

Remember to exclude the Jack Pearson himself from the result!