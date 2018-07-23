## Instruction
Excellent! These examples are getting too easy for you! Let's try something more complicated.

So far, our subqueries only returned single values (like 5 or 15.28 for example). Let's change that.

First, we need to learn a new operator. Take a look at the example:

````sql
SELECT * FROM city WHERE rating IN (3,4,5);
````

Can you guess what IN means? That's right, it allows you to specify a few values in the WHERE clause instead of just one.

In our example, we only want to show interesting cities, but we're not very picky - any city with the rating 3 OR 4 OR 5 will do. That's what IN (3,4,5) means.

---
## Exercise
Find all information about hiking trips with difficulty 1, 2 or 3.