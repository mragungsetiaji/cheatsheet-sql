## Instruction
Excellent! As you could see, the same table was used twice to apply the join. This is why Jack Pearson was also shown together with Jack Pearson. The database won't check whether the 2 people in the match are the same unless you tell it to do so.

You can add another condition in the WHERE clause:

````sql
SELECT * FROM student AS s1 
JOIN student AS s2 
ON s1.room_id = s2.room_id 
WHERE s1.name = 'Jack Pearson' 
AND s1.name != s2.name;
````
Thanks to the second condition, Jack Pearson won't be shown together with himself.

You can also use more than one join in your SQL instruction. Let's say we also want to show all the room information for the student pairs with Jack Pearson. Unfortunately, data like room number or floor is not stored in the table student - we need yet another join with the table room:

````sql
SELECT * 
FROM student AS s1 
JOIN student AS s2 ON s1.room_id = s2.room_id 
JOIN room ON s2.room_id = room.id 
WHERE s1.name = 'Jack Pearson' 
AND s1.name != s2.name;
````

Now that you know self-joins and joining more than 2 tables, we have a tiny challenge for you.

---
## Exercise
The challenge is as follows: for each room with 2 beds where there actually are 2 students, we want to show one row which contains the following columns:

- the name of the first student,
- the name of the second student and
- the room number.

Don't change any column names. Each pair of students should only be shown once. The student whose name comes first in the alphabet should be shown first.
A small hint: in terms of SQL, "first in the alphabet" means "smaller than" for text values.