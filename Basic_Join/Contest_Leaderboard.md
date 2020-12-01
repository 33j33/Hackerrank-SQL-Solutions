## Link 

https://www.hackerrank.com/challenges/contest-leaderboard/problem

## Solution

```sql
SELECT h.hacker_id, name, SUM(score) AS total_score
FROM
hackers AS h
INNER JOIN
/* find max_score*/
(SELECT hacker_id,  MAX(score) AS score FROM submissions GROUP BY challenge_id, hacker_id)
AS max_score

/*Do join of hackers and max_score */
ON h.hacker_id=max_score.hacker_id
GROUP BY h.hacker_id, name

/* don't accept hackers with total_score=0 */
HAVING total_score > 0

/* finally order as required */
ORDER BY total_score DESC, h.hacker_id
;
```