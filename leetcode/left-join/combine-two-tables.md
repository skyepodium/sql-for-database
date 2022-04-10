# 1. 설명
두개의 테이블을 결합한 결과를 반환하세요


[문제 링크](https://leetcode.com/problems/combine-two-tables/)


# 2. 코드
### 1) MySql
```sql
SELECT
        p.firstName
    ,   p.lastName
    ,   a.city
    ,   a.state
FROM 
    Person as p
        LEFT JOIN
    Address as a
        ON p.personId = a.personId
```

### 2) Oracle
```sql
SELECT
        p.firstName
    ,   p.lastName
    ,   a.city
    ,   a.state
FROM 
    Person p
        LEFT JOIN
    Address a
        ON p.personId = a.personId
```