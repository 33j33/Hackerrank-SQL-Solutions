#### LINK

https://www.hackerrank.com/challenges/weather-observation-station-12/problem

#### SOLUTION

```sql
SELECT DISTINCT city
FROM station 
WHERE city REGEXP "^[^aeiouAEIOU].*[^aeiouAIEOU]$"

-- `.` is representing one character and `..` is representing two characters and so
--  `.*` is representing as many characters u want

-- [^aeiou] -> should not match any character aeiou

-- ^[^aeiou] -> should not match first character with aeiou

-- The ^ in brackets negates.

-- [^aeiou]$ -> should not match last character with aeiou
```