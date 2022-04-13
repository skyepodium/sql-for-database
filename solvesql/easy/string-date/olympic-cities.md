# 1. 설명
2000년 이상, 올림픽 년도 내림차순, 도시명 3글자 대문자

[문제 링크](https://solvesql.com/problems/order-by/)


# 2. 코드
### 1) SQLite
```sql
SELECT
    YEAR
  , UPPER(SUBSTR(CITY, 1, 3)) AS CITY
FROM 
  GAMES
WHERE
  YEAR >= 2000
ORDER BY
  YEAR DESC

```
