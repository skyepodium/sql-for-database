# 1. 설명
팁을 가장 많이 받을 수 있는 날을 구하세요

[문제 링크](https://solvesql.com/problems/best-working-day/)


# 2. 코드
### 1) SQLite
```sql
SELECT
    DAY
  , SUM(TIP) tip_daily
FROM
  TIPS
GROUP BY
  DAY
ORDER BY 
  tip_daily DESC
limit 1
```
