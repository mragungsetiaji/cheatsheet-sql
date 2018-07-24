## Instruction
This quiz is too easy for you! OK, let's see how much you remember about various JOINs.

`player (id, name, ranking, country)`

`coach (id, player_id, name, country)`

We now have two tables with tennis players and their coaches. Each player can have one or more coaches. Each coach can train one player or can be unemployed.

The columns should be obvious for you.

---
## Exercise
Show alll coaches together with the players they train, show all columns for coaches and players. Show unemployed coaches with NULLS instead of player data.