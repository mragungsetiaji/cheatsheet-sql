## Instruction
Great. NATURAL JOIN doesn't require column names because it always joins the two tables on the columns with the same name.

In our example, students and rooms have been joined on the column id, which doesn't really make much sense.

In our dormitory, the construction

````sql
SELECT * FROM student NATURAL JOIN room;
gives the same result as the following query:
SELECT * FROM student JOIN room 
ON student.id = room.id;
````

You can, however, construct your tables in such a way that NATURAL JOIN comes in handy. If you had the following tables:

> `car(car_id, brand, model);`

> `owner(owner_id, name, car_id);`

then it would make perfect sense to use NATURAL JOIN because it would join the two tables on the column car_id. You would then need fewer keyboard strokes to join two tables.

---
## Exercise
Next exercise to continue.