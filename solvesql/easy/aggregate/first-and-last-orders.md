# 1. 설명
첫주문일, 마지막 주문일 조회

[문제 링크](https://solvesql.com/problems/first-and-last-orders/)


# 2. 코드
### 1) SQLite
```sql
SELECT
    DATE(MIN(ORDER_PURCHASE_TIMESTAMP)) FIRST_ORDER_DATE
  , DATE(MAX(ORDER_PURCHASE_TIMESTAMP)) LAST_ORDER_DATE
FROM
  OLIST_ORDERS_DATASET
```
