# 1. 설명
상위 N개의 레코드를 조회하세요

[문제 링크](https://programmers.co.kr/learn/courses/30/lessons/59405)


# 2. 코드
### 1) MySql
```sql
SELECT 
    NAME
FROM 
    ANIMAL_INS
ORDER BY 
    DATETIME ASC
LIMIT 1
```

### 2) Oracle
```sql
SELECT 
    *
FROM 
    (
        SELECT
            NAME
        FROM 
            ANIMAL_INS
        ORDER BY 
            DATETIME ASC
    )
WHERE 
    ROWNUM <= 1
```