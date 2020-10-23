#### LINK

https://www.hackerrank.com/challenges/the-pads/problem

#### SOLUTION

```sql

SELECT CONCAT(name, "(", LEFT(occupation, 1), ")") 
FROM occupations
ORDER BY name;

SELECT CONCAT("There are a total of ", COUNT(*), " ", LOWER(occupation), "s.")
FROM occupations
GROUP BY occupation
ORDER BY COUNT(*), occupation
-- The items are grouped by occupation and count of each occupation is totalled
-- The GROUP BY clause is an optional clause of the SELECT statement that combines rows into groups based -- on matching values in specified columns. One row is returned for each group.

-- You often use the GROUP BY in conjunction with an aggregate function such as MIN, MAX, AVG, SUM, or COUNT to calculate a measure that provides the information for each group.
```
https://www.geeksforgeeks.org/sql-group-by/

https://www.w3schools.com/sql/sql_groupby.asp

https://www.sqltutorial.org/sql-group-by/
