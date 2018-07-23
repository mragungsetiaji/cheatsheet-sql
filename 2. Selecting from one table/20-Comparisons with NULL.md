## Instruction
Good job. Remember, `NULL` is a special value. It means that some piece of information is **missing** or **unknown**.

If you set a condition on a particular column, say `AGE < 70`, the rows where age is `NULL` will always be **excluded** from the results. Let's check that in practice.

In no way does `NULL` equal zero. What's more, the expression `NULL = NULL` is never true in SQL!

---
## Exercise
Select all columns for cars whose price column is greater than or equal to zero.

Note that the Opel with an unknown price is not in the result.