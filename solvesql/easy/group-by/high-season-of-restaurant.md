# 1. 설명
결제 금액이 1500 이상인 요일의 모든 데이터를 조회하세요

[문제 링크](https://solvesql.com/problems/high-season-of-restaurant/)


# 2. 코드
### 1) SQLite
```sql
SELECT
  *
FROM
  TIPS
WHERE
  DAY IN (
    SELECT
      DAY
    FROM
      TIPS
    GROUP BY
      DAY
    HAVING
      SUM(TOTAL_BILL) >= 1500
  )
```
