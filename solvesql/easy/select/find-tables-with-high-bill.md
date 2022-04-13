# 1. 설명
결제 금액이 평균 보다 큰 비용을 구하세요

[문제 링크](https://solvesql.com/problems/find-tables-with-high-bill/)


# 2. 코드
### 1) SQLite
```sql
SELECT
  *
FROM
  TIPS
WHERE
  TOTAL_BILL > (
    SELECT
      AVG(TOTAL_BILL) AVG_BILL
    FROM
      TIPS
  )
```
