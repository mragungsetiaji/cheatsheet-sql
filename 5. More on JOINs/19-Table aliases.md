## Instruction
Speaking of fewer keyboard strokes, there is one more thing which may come in handy and make you write less: aliases for tables.

Imagine the following situation: we want to select many columns from two joined tables. You could, of course, write it like this:

````sql
SELECT person.id, person.name,
       person.year, car.id,
       car.name, car.year 
FROM person JOIN car 
ON person.id = car.owner_id;
````

Takes a lot of writing, doesn't it? All those column names together with their table names... Fortunately, there is a way to make things simpler: we can introduce new temporary names (called aliases) for our tables:

````sql
SELECT p.id, p.name, p.year, 
       c.id, c.name, c.year 
FROM person AS p 
JOIN car AS c 
ON p.id = c.owner_id;
````

As you can see, after the table names in the FROM clause we used the keyword AS. It indicates that whatever comes next will become the new, temporary name (alias) for the table. Thanks to it, we could save our fingers a little bit and write shorter names for our tables.

---
## Exercise
Use INNER JOIN on the tables room and equipment so that all pieces of equipment are shown their rooms. Use table aliases r and e. Select the columns id and name from the table equipment as well as room_number and beds from the table room.