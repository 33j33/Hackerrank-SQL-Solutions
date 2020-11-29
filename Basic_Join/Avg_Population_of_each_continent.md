## Link

https://www.hackerrank.com/challenges/average-population-of-each-continent/problem


## Solution

```sql
SELECT country.continent, FLOOR(AVG(city.population))
FROM city, country
WHERE city.countrycode = country.code
GROUP BY country.continent
```
or

```sql
SELECT country.continent, FLOOR(AVG(city.population))
FROM city
JOIN country
ON city.countrycode = country.code
GROUP BY country.continent
```
- https://www.sqltutorial.org/sql-group-by/
- https://www.w3schools.com/sql/sql_groupby.asp
