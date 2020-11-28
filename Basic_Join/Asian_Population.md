### Link

https://www.hackerrank.com/challenges/asian-population/problem

### Solution

Use WHERE to do natural join
```sql
SELECT SUM(city.population)
FROM city, country
WHERE city.countrycode = country.code and continent = 'Asia'
```

OR 
You can use JOIN to do the natural join
```sql
SELECT SUM(city.population)
FROM city
JOIN country
ON city.countrycode = country.code
WHERE continent = 'Asia'
```