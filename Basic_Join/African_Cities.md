## Link 

https://www.hackerrank.com/challenges/african-cities/problem

## Solution

```sql
SELECT city.name
FROM city, country
WHERE city.countrycode = country.code AND continent = 'Africa'
```

```sql
SELECT city.name
FROM city
JOIN country
ON city.countrycode = country.code
WHERE continent = 'Africa'
```