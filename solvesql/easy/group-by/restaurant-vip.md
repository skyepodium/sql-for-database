# 1. 설명
요일별 거래 금액이 가장 큰 데이터를 조회하세요

[문제 링크](https://solvesql.com/problems/restaurant-vip/)


# 2. 코드
### 1) SQLite
```sql
SELECT 
  *
FROM 
  TIPS
GROUP BY
  DAY
HAVING
  TOTAL_BILL = MAX(TOTAL_BILL)
```
