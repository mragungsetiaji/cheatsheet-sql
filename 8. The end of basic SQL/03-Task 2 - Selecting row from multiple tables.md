## Instruction
Wow, excellent! You remember Part 1 very well!

Now, let's see if you can still recall how to work with more than one table. Let's analyze the next situation:

`pet (id, owner_id, name, type, year_born)`

`owner (id, name, year_born)`

In this task, our small database collects information about pets and their owners in two separate tables.

Each pet has an id, is assigned to a specific owner, has a name, is of certain type (dog, cat, ...) and was born in a specific year.

Each owner has an id, a name and, again, was born in a specific year.

----
## Exercise
Show all pets (show the columns name, type, year_born) whose name begins with an 'M' together with their owners (the columns name, year_born).

Rename the column year_born from the table pet as pet_year_born and the column year_born from the table owner as owner_year_born.