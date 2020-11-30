## Link

https://www.hackerrank.com/challenges/weather-observation-station-17/problem

## Solution

```sql
SELECT ROUND(long_w, 4)
FROM station
WHERE lat_n > 38.7780
ORDER BY lat_n ASC
LIMIT 1
```

Note we can use nested select query as well to solve this problem

