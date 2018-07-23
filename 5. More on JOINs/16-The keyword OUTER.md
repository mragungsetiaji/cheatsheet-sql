## Instruction
OK. Remember when we told you that JOIN is short for INNER JOIN?

The three joins we mentioned just now: LEFT JOIN, RIGHT JOIN and FULL JOIN are also shortcuts of some kind. They are all actually OUTER JOINS: LEFT OUTER JOIN, RIGHT OUTER JOIN and FULL OUTER JOIN. You can add the keyword OUTER and the results of your queries will stay the same.

For example, for the LEFT JOIN, you could just as well write:

````sql
SELECT * 
FROM person 
LEFT OUTER JOIN car 
ON person.id = car.owner_id;
````

## Exercise
Check it our for yourself. Use the full name RIGHT OUTER JOIN to show all the kettles together with their rooms (even if there is no room assigned).