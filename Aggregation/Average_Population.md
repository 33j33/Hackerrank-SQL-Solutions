#### LINK

https://www.hackerrank.com/challenges/average-population/problem

#### SOLUTION

```sql
SELECT ROUND(AVG(population))
FROM city
```

**`ROUND(number, decimals)`**

1. number - Required. The number to be rounded
2. decimals -	Optional. The number of decimal places to round number to. If omitted, it returns the integer (no decimals)

https://www.w3schools.com/sql/func_mysql_avg.asp

https://www.w3schools.com/sql/func_mysql_round.asp