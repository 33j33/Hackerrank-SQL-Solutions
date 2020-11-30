## Link

https://www.hackerrank.com/challenges/weather-observation-station-20/problem

## Solution 

```sql
SELECT ROUND(S.LAT_N, 4) FROM STATION S 
    WHERE 
        (SELECT COUNT(LAT_N) FROM STATION WHERE LAT_N > S.LAT_N) 
        = (SELECT COUNT(LAT_N) FROM STATION WHERE LAT_N < S.LAT_N);
```

The below solution doesn't work because you can't call a function on the LIMIT clause like that. It expects a non-negative count of type INT64 (https://cloud.google.com/bigquery/docs/reference/standard-sql/query-syntax#limit_and_offset_clause)

```sql
SELECT ROUND(lat_n, 4)
FROM (
    SELECT * 
    FROM station as s
    ORDER BY lat_n DESC
    LIMIT FLOOR(COUNT(s.id)/2)
)
LIMIT 1;
```