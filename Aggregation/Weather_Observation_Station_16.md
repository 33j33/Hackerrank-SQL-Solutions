## Link

https://www.hackerrank.com/challenges/weather-observation-station-16/problem

## Solution

```sql
SELECT ROUND(MIN(lat_n), 4)
FROM station
WHERE lat_n > 38.7780
```
