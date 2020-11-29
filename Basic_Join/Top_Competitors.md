## Link 

https://www.hackerrank.com/challenges/full-score/problem

## Solution

```sql
SELECT h.hacker_id, h.name
FROM submissions AS s
JOIN challenges AS c
    ON s.challenge_id = c.challenge_id
JOIN difficulty AS d
    ON c.difficulty_level = d.difficulty_level 
JOIN hackers AS h
    ON s.hacker_id = h.hacker_id
WHERE s.score = d.score 
GROUP BY h.hacker_id, h.name
HAVING COUNT(s.hacker_id) > 1
ORDER BY COUNT(s.hacker_id) DESC, s.hacker_id ASC
```
#### Explaination

/* join tables together, to make a master table which contains all the info */ 
```sql
SELECT h.hacker_id, h.name
FROM submissions AS s
JOIN challenges AS c
    ON s.challenge_id = c.challenge_id
JOIN difficulty AS d
    ON c.difficulty_level = d.difficulty_level 
JOIN hackers AS h
    ON s.hacker_id = h.hacker_id
```
/* filter logic, to eliminate submissions that did not earn full score */ 
```sql
WHERE s.score = d.score
```

/* further eliminate hackers who only had one full-score submission */ 
```sql
GROUP BY h.hacker_id, h.name
HAVING COUNT(s.hacker_id) > 1
```
Why `h.name` is included in the 'GROUP BY' is explained here 

https://stackoverflow.com/questions/13999817/reason-for-column-is-invalid-in-the-select-list-because-it-is-not-contained-in-e/13999903#13999903

/* display by the order stated in the proble, */
```sql
ORDER BY COUNT(s.hacker_id) DESC, s.hacker_id ASC
```