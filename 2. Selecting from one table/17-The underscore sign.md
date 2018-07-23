## Instruction
Nice! Now, sometimes we may not remember just one letter of a specific name. Imagine we want to find a girl whose name is... Catherine? Katherine?

> `SELECT * 
FROM user 
WHERE name LIKE '_atherine';`

The underscore sign (`_`) replaces exactly one character. Whether it's Catherine or Katherine - the expression will return a row.

---
## Exercise
Select all columns for cars whose brand is 'Volk_wagen' (the underscore replaces one unknown characters).