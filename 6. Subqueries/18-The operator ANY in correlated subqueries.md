## Instruction
Okay! One more thing - you can also use the operator ANY in your correlated subqueries. Just take a look:

```SQL
SELECT * FROM hiking_trip 
WHERE price < ANY (SELECT price FROM trip 
   WHERE trip.days = hiking_trip.days);
```

The above query compares city trips and hiking trips which last the same number of dates. It then returns all hiking trips which are cheaper than any city trip of the same duration time.

---
## Exercise
Select those trips which last shorter than any hiking_trip with the same price.