#### LINK

https://www.hackerrank.com/challenges/more-than-75-marks/problem

#### SOLUTION

```sql
SELECT name
FROM students
WHERE marks > 75
ORDER BY RIGHT(name, 3), id
-- The RIGHT() function extracts a number of characters from a string (starting from right).
```