## Instruction
Excellent! Now, you should be aware that JOIN is actually just one of a few joining methods. It's the most common one so it's always applied by default when you write the keyword JOIN in your SQL statement. Technically speaking, though, its full name is INNER JOIN.

The example from the previous exercise can be just as well written in the following way:

```SQL
SELECT * 
FROM person 
INNER JOIN car 
ON person.id = car.owner_id;
```

## Exercise
Now, use the full name INNER JOIN to join the tables room and equipment so that each piece of equipment is shown together with its room.