## Link

https://www.hackerrank.com/challenges/the-report/problem

## Solution 

```sql
SELECT IF (Grades.Grade > 7, Students.Name, NULL) AS Sname, Grades.Grade, Students.Marks
FROM Students 
INNER JOIN Grades
ON Students.Marks BETWEEN Grades.Min_Mark AND Max_Mark
ORDER BY Grades.Grade DESC, Sname ASC, Students.Marks ASC;
```

https://www.w3schools.com/sql/func_mysql_if.asp