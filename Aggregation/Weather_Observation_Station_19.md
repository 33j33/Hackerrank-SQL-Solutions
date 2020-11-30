## Link

https://www.hackerrank.com/challenges/weather-observation-station-19/problem

## Solution

```sql
SELECT TRUNCATE(SQRT((POW(MAX(lat_n) - MIN(lat_n), 2) + POW(MAX(long_w) - MIN(long_w), 2))), 4)
FROM station
```

In a plane with p1 at `(x1, y1)` and p2 at `(x2, y2)`, it is `sqrt((x1 - x2)^2 + (y1 - y2)^2)`