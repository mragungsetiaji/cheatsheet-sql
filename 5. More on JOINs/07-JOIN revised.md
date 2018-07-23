## Instruction
Good, let's get started!

Do you still remember how we joined two tables in Part 2 of our SQL course? Let's revise the example we gave for people and their cars:

```SQL
SELECT * 
FROM person 
JOIN car 
ON person.id = car.owner_id;
```
That's right, we put the keyword JOIN between the names of two tables and then, after another keyword ON, we provided the condition.

In this particular example, we joined the rows where value of the column owner_id (table car) was identical with the value of the column id (table person). In this way, we joined cars with their owners.

---
## Exercise
Try it yourself. Join the two tables: student and room so that each student is shown together with the room they live in. Select all columns.

