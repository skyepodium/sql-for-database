# 1. 설명
피자를 주문한적이 없는 고객을 조회하세요


[문제 링크](https://leetcode.com/problems/customers-who-never-order/)

# 참고
MySql은 `not in`이 더 빠르고
Oracle은 `left join`이 더 빨랐습니다.


# 2. 코드
### 1) MySql
- left join
```sql
SELECT 
    C.name as Customers
FROM
    Customers as C
        LEFT JOIN
    Orders as O
        on C.id = O.customerId
WHERE
    O.customerId is null
```

- not in
```sql
SELECT 
    C.name as Customers
FROM
    Customers as C
WHERE
    C.id not in (
        SELECT 
            customerId 
        FROM 
            Orders
    )
```


### 2) Oracle
- left join
```sql
SELECT 
    C.name as Customers
FROM
    Customers C
        LEFT JOIN
    Orders O
        on C.id = O.customerId
WHERE
    O.customerId is null
```

- not in
```sql
SELECT 
    C.name as Customers
FROM
    Customers C
WHERE
    C.id not in (
        SELECT 
            customerId 
        FROM 
            Orders
    )
```