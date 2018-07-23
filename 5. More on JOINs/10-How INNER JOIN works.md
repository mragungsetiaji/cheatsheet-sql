## Instruction
Good. If you now compare the results of INNER JOIN with the content of the equipment table (expand the Database tab on the right), you'll notice that not all pieces of equipment are present in the resulting table. For example, a lovely kettle with the id 11 is not there. Do you know why?

INNER JOIN (or JOIN, for short) only shows those rows from the two tables where there is a match between the columns. In other words, you can only see those pieces of equipment which have a room assigned and vice versa. Equipment with no room is not shown in the result. Take a look at the table:


> `equipment` (for column 1->3) and the rest is `room`

|ID|NAME|ROOM_ID|ID|ROOM_NUMBER|BEDS|FLOOR|
|---|---|---|---|---|---|---|
|1|kettle|4|4|104|3|1|
|2|fridge|5|5|201|1|2|
|3|tv|8|8|204|3|2|
|5|kettle|7|7|203|3|2|
|6|radio|7|7|203|3|2|
|7|computer|7|7|203|3|2|
|8|toaster|1|1|101|2|1|
|9|toaster|1|1|101|2|1|
|12|kettle|2|2|102|2|1|
|13|tv|3|3|103|3|1|
|14|microwave|9|9|205|4|2|
|15|computer|10|10|301|4|3|
|4|tv|null|||||	 	 	 	 
|10|microwave|null|||||	 	 	 	 
|11|kettle|null|||||	 	 	 	 
 

The rows marked in green are the result of the INNER JOIN. Equipment with NULL value in the room_id table, marked in red, is NOT shown in the INNER JOIN result.

---
## Exercise
Next exercise to continue.