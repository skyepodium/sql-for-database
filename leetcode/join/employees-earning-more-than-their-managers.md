# 1. 설명
자신의 매니저보다 많이 받는 직원을 조회하세요


[문제 링크](https://leetcode.com/problems/employees-earning-more-than-their-managers/)


# 2. 코드
### 1) MySql
```sql
SELECT 
    a.name as Employee
FROM
    Employee as a
        INNER JOIN
    Employee as b
        on a.managerId = b.id
        AND a.salary > b.salary
    
```

### 2) Oracle
```sql
SELECT 
    a.name as Employee
FROM
    Employee a
        INNER JOIN
    Employee b
        on a.managerId = b.id
        AND a.salary > b.salary
```