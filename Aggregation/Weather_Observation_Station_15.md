## Link

https://www.hackerrank.com/challenges/weather-observation-station-15/problem

## Solution 

Using Nested Query
```sql
SELECT ROUND(long_w, 4)
FROM station
WHERE lat_n = (SELECT MAX(lat_n) FROM station WHERE lat_n < 137.2345)
```

OR

```sql
SELECT ROUND(LONG_W, 4)
FROM STATION
WHERE LAT_N < 137.2345
ORDER BY LAT_N DESC
LIMIT 1;
```
