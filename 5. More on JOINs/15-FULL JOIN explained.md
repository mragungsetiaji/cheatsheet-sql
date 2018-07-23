Instruction
Excellent. Another joining method is FULL JOIN. This type of JOIN returns all rows from both tables and combines the rows when there is a match. In other words, FULL JOIN is a union of LEFT JOIN and RIGHT JOIN.

Let's see an example:

````sql
SELECT *
FROM car
FULL JOIN person
ON car.owner_id = person.id;
````
The result may look like this:

> `car` (column 1-->3) and the rest `person`

|ID|BRAND|OWNER_ID|ID|NAME|
|---|---|---|---|---|
|1|Ford|3|3|Megan Donald|
|2|Opel|5|5|John Smith|
|3|Nissan|4|4|Andrew Black|
|4|Skoda|null|null|null|
|5|BMW|null|null|null|
|6|Citroen|null|null|null|
|null|null|null|1|Sylvia Green|
|null|null|null|2|Martin Dean|
|null|null|null|6|Adam Scott|

The red rows are the rows returned by INNER JOIN. The green rows are the rows which would be added by a LEFT JOIN and the purple rows are the rows which would be added by a RIGHT JOIN.
A FULL JOIN returns ALL rows in the table above.

Unfortunately, some databases don't support FULL JOINs and this is exactly the problem with the database we're working on in this SQL course. In other words, we'll let you off without an exercise this time!

---
## Exercise
Next exercise to continue.