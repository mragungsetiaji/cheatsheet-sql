## Instruction
Until now, we only worked with numbers in our `WHERE` clauses. Is it possible to put letters in their place? Of course it is! Just remember to put your text in single quotes like this: `'example'`.

If you wanted to know the age of all Smiths in your table, you could use the following code:

> `SELECT age from user 
WHERE name = 'Smith';`

Note that the case of the letters matters, i.e. 'Smith' is different than 'SMITH'.

---
## Exercise
Select all columns of all Ford cars from the table.