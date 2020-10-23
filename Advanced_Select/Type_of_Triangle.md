#### LINK

https://www.hackerrank.com/challenges/what-type-of-triangle/problem

#### SOLUTION

```sql
SELECT 
CASE
    WHEN A >= B + C OR B >= A + C OR C >= B + A THEN "Not A Triangle"
    WHEN A = B AND B = C THEN "Equilateral"
    WHEN A = B OR C = A OR C = B THEN "Isosceles"
    ELSE "Scalene"
END
FROM TRIANGLES
-- The CASE statement goes through conditions and returns a value when the first condition is met (like an IF-THEN-ELSE statement). So, once a condition is true, it will stop reading and return the result. If no conditions are true, it returns the value in the ELSE clause. 
```

[SQL CASE statement] https://www.w3schools.com/sql/sql_case.asp

