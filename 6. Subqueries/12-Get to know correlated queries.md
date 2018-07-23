## Instruction
Very good. So far, we've only used subqueries which were independent of the main query - you could first run the subquery alone and then put its result in the main query.

We are now going to learn subqueries which are dependent on the main query. They are called correlated subqueries.

Study the example:

````SQL
SELECT * FROM country 
WHERE area <= (SELECT min(area) 
FROM city 
WHERE city.country_id = country.id);
````

We want to find all countries whose area is equal to or smaller than the minimum city area in that particular country. In other words, if there is a country smaller than its smallest city, it will be shown. Why would we use such a query? It can be very convenient if we want to check whether there any are errors in our database. If this query returned anything else than nothing, we would know that something fishy is going on in our records.

What's the new piece here? Take a look at the WHERE clause in the subquery. That's right, it uses country.id. Which country does it refer to? The country from the main clause of course. This is the secret behind correlated subqueries - if you ran the subquery alone, your database would say 
'Hey, you want me to compare city.country_id to country.id, but there are tons of ids in the table country, so I don't know which one to choose'.
But if you run the instruction as a subquery and the main clause browses the table country, then the database will each time compare country.id from the subquery with the current country.id from the main clause.

Just remember the golden rule: subqueries can use tables from the main query, but the main query can't use tables from the subquery!

---
## Exercise
Let's check if the database contains any errors in another way.

Find all information about each country whose population is equal to or smaller than the population of the least populated city in that specific country.