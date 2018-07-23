## Instruction
Great. As you may have guessed, there is also a RIGHT JOIN.

The RIGHT JOIN works in the following way: it returns ALL rows from the right table (the second table in the query) plus all matching rows from the left table (the first table in the query).

Let's see an example. Take a look at the query:

````sql
SELECT *
FROM car 
RIGHT JOIN person
ON car.owner_id = person.id;
````

RIGHT JOIN result is shown in the following table:

> `car` (column 1-->3) and the rest is `person`

|ID|BRAND|OWNER_ID|ID|NAME|
|---|---|---|---|---|
|1|Ford|3|3|Jane Preston|
|2|Opel|1|1|Cody Wright|
|3|Volkswagen|2|2|Oscar Walls|
|4|Toyota|4|4|Megan Black|
|null|null|null|5|Alice Cooper|
|null|null|null|6|James Brown|
|null|null|null|7|Charles Smith|

The RIGHT JOIN returns all rows in the table above. The red rows are the rows returned by an INNER JOIN. The green rows are the rows added by a RIGHT JOIN.

Notice that the order of the tables in LEFT and RIGHT JOIN does matter. In other words, car RIGHT JOIN person is the same as person LEFT JOIN car. Don't confuse the order!

---
## Exercise
For each student show student data and a room the student lives in. Show also rooms with no students assigned. Use a RIGHT JOIN.