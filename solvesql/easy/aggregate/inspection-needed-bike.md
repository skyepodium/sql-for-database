# 1. 설명
2021-01 한달 주행 거리가 50km 이상인 자전가 ID 조회

[문제 링크](https://solvesql.com/problems/inspection-needed-bike/)


# 2. 코드
### 1) SQLite
```sql
SELECT
  BIKE_ID
FROM
  RENTAL_HISTORY
WHERE 
  RENT_AT >= '2021-01' 
  AND RENT_AT <= '2021-02'
GROUP BY
  BIKE_ID
HAVING
  SUM(DISTANCE) >= 50000
```
