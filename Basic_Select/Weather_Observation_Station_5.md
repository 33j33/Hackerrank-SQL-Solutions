#### LINK 

https://www.hackerrank.com/challenges/weather-observation-station-5/problem

#### SOLUTION

```sql
SELECT CITY, LENGTH(CITY) 
FROM STATION 
WHERE LENGTH(CITY) <= ALL(
SELECT LENGTH(CITY)
FROM STATION
)
ORDER BY CITY
LIMIT 1;

SELECT CITY, LENGTH(CITY)
FROM STATION
WHERE LENGTH(CITY) >= ALL(
SELECT LENGTH(CITY)
FROM STATION
)
ORDER BY CITY
LIMIT 1
```

---

**Better Solution**

```sql
SELECT city, LENGTH(city)
FROM station
ORDER BY LENGTH(city), city ASC
LIMIT 1;


SELECT city, LENGTH(city)
FROM station
ORDER BY LENGTH(city) DESC, city
LIMIT 1;
```