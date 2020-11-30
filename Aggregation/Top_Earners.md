## Link

https://www.hackerrank.com/challenges/earnings-of-employees/problem

## Solution

```sql
SELECT months*salary as earnings, COUNT(*)
FROM employee
GROUP BY earnings
ORDER BY earnings DESC
LIMIT 1
```