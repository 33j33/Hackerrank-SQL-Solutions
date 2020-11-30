## Link

https://www.hackerrank.com/challenges/weather-observation-station-13/problem

## Solution 

```sql
SELECT TRUNCATE(SUM(lat_n), 4)
FROM station
WHERE lat_n BETWEEN 38.788 AND 137.2345
```

https://www.w3schools.com/sql/func_mysql_truncate.asp

