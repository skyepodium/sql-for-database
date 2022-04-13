# 1. 설명
총 주문이 100건 이상인 판매자를 조회하세요

[문제 링크](https://solvesql.com/problems/settled-sellers-1/)


# 2. 코드
### 1) SQLite
```sql
SELECT
    SELLER_ID
  , COUNT(DISTINCT ORDER_ID) ORDERS
FROM 
  OLIST_ORDER_ITEMS_DATASET
GROUP BY
  SELLER_ID
HAVING
  COUNT(DISTINCT ORDER_ID) >= 100
```
