# 1. 설명
중복된 이메일을 반환하세요

[문제 링크](https://leetcode.com/problems/duplicate-emails/)


# 2. 코드
### 1) MySql
```sql
SELECT 
    EMAIL
FROM 
    Person
GROUP BY
    EMAIL
HAVING
    COUNT(EMAIL) >= 2
```

### 2) Oracle
```sql
SELECT 
    EMAIL
FROM 
    Person
GROUP BY
    EMAIL
HAVING
    COUNT(EMAIL) >= 2
```