## Instruction
Great. In the previous example, we provided column names together with the tables they are a part of. It's good practice, but you only **need** to do it when there is **a chance to confuse them**. If there are two different columns under the same name in two different tables, then you have to specify the tables. **If the name of the column is unique, though, you may omit the table name.**

````sql
SELECT name, model 
FROM person JOIN car 
ON person.id = owner_id;
````

There is only one column named `name` and one only column named `model` in the tables person, car, so we could provide their names without giving information about the tables they come from. Similarly, there is only one column named `owner_id` - it is only in the table `car`, so we can omit the name of the table.

When we refer to column `id` from table `person`, though, we must write the table name as well (`person.id`), because there is another column under the name `id` in table `car`.

---
## Exercise
Select **director name** and **movie title** from tables `movie` and `director` in such a way that a movie is shown together with its director. Use as few characters as possible.