## Instruction
OK, we'll now learn a new kind of JOIN: LEFT JOIN.

LEFT JOIN works in the following way: it returns ALL rows from the left table (the first table in the query) plus all matching rows from the right table (the second table in the query).

Let's see an example

````SQL
SELECT *
FROM car
LEFT JOIN person
ON car.owner_id = person.id;
````

The result may look like this:

> `car` (for column 1-->3) and the rest is `person`

|ID|BRAND|OWNER_ID|ID|NAME|
|---|---|---|---|---|
|1|Ford|3|3|Jane Preston|
|2|Opel|1|1|Cody Wright|
|3|Volkswagen|2|2|Oscar Walls|
|4|Toyota|4|4|Megan Black|
|5|Citroen|null		
|6|Nissan|null		
|7|Skoda|null

The LEFT JOIN returns ALL rows in the above table. The red rows are the rows returned by INNER JOIN. The green rows are the rows added by a LEFT JOIN: there is no matching owner for the green cars but a LEFT JOIN returns them nevertheless.

---
## Exercise
Show all rows from the table student. If a student is assigned to a room, show the room as well.