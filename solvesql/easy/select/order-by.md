# 1. 설명
QUARTET = 'I', Y 오름차순

[문제 링크](https://solvesql.com/problems/order-by/)


# 2. 코드
### 1) SQLite
```sql
SELECT
  *
FROM
  POINTS
WHERE
  QUARTET = 'I'
ORDER BY
  Y ASC
```
