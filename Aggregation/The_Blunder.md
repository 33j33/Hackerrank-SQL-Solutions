## Link

https://www.hackerrank.com/challenges/the-blunder/problem

## Solution 

```sql
SELECT CEIL(AVG(Salary)-AVG(REPLACE(Salary,'0','')))
FROM EMPLOYEES;
```

https://www.w3schools.com/sql/func_mysql_replace.asp
