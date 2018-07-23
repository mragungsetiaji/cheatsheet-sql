## Instruction
Good job! We can do one more thing with our columns: rename them. Up till now, the column named `id` was always shown as `id` in the result. Now we can change it:

````sql
SELECT person.id AS person_id, car.id AS car_id 
FROM person JOIN car 
ON person.id = car.owner_id;
````

After the column name, e.g. `person.id`, we use the new keyword `AS` and we put the new name after it (`person_id`). We can repeat this process with every column.

The new name is just an **alias**, which means it's temporary and doesn't change the actual column name in the database. It only influences the way the column is shown in the result of the specific query. This technique is often used when there are a few columns under the same name coming from different tables. Normally, when SQL displays columns in the result, there is no information about the table that a specific column is part of.

In our example, we had two columns `id`, so we renamed them to `person_id` and `car_id` respectively. Now, if we see the columns in the result, we will know which column comes from which table.

---
## Exercise
Select **director name** and **movie title** from tables `movie` and `director` in such a way that a movie is shown together with its director. Rename the column `title` to `movie_title`.