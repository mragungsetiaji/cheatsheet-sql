## Instruction
Outstanding! Since you're doing so well, you should be ready for another operator. See the example:

````sql
SELECT * FROM country 
WHERE area > ALL (SELECT area FROM city);
````

As you can see, we've got a new operator ALL on the right side of the logical operator >. In this case, > ALL means 'greater than every other value from the brackets'.

As a result, we'll get all the countries whose area is bigger than every other area of all cities. Liechtenstein, for instance, is a very small country. It is bigger than some cities (like Lyon, for example), but it is not bigger than every other city (Berlin is bigger, for example) so it won't be shown in the result.

You can also use ALL with other logical operators: = ALL, =! ALL, < ALL, <= ALL, >= ALL.

---
## Exercise
Find all information about the cities which are less populated than all countries in the database.