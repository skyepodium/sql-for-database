# 1. 설명
Recyclable, Low Fat 상품을 조회하세요


[문제 링크](https://leetcode.com/problems/recyclable-and-low-fat-products/)


# 2. 코드
### 1) MySql
```sql
SELECT 
    PRODUCT_ID
FROM 
    PRODUCTS
WHERE
    LOW_FATS = 'Y'
        AND
    RECYCLABLE = 'Y'

```

### 2) Oracle
```sql
SELECT 
    PRODUCT_ID
FROM 
    PRODUCTS
WHERE
    LOW_FATS = 'Y'
        AND
    RECYCLABLE = 'Y'

```