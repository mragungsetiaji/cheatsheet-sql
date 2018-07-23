## Instruction
Very well!

You can select some columns in a JOIN query. Take a look at the example:

```SQL
SELECT person.name, car.brand, car.model 
FROM person 
JOIN car
ON person.id = car.owner_id;
```
Instead of all columns (select with the asterisk *) here we select only three columns: name from table person, brand from table car and model from table car.

We first put the name of the table, then a dot ., and then the name of the column we want to select.

---
## Exercise
Join tables: student and room so that each student is shown together with the room they live in.

Select the name of the student and room number.