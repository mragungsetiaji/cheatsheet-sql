## Instruction
There's one more joining method before you go. It's called NATURAL JOIN and it's slightly different from the other methods because it doesn't require the ON clause with the joining condition:

```sql
SELECT * FROM person 
NATURAL JOIN car;
```
Check it yourself and try to guess how it works.

---
## Exercise
Use NATURAL JOIN on the tables student and room.