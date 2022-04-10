# 1. 설명
null 이면 'No name' 으로 변경 후 조회하세요

[문제 링크](https://programmers.co.kr/learn/courses/30/lessons/59410)


# 2. 코드
### 1) MySql
```sql
SELECT
        ANIMAL_TYPE
    ,   CASE
            WHEN NAME IS NOT NULL THEN NAME
        ELSE
            'No name'
        END AS NAME
    ,   SEX_UPON_INTAKE
FROM 
    ANIMAL_INS
ORDER BY
    ANIMAL_ID ASC
```

### 2) Oracle
```sql
SELECT
        ANIMAL_TYPE
    ,   CASE
            WHEN NAME IS NOT NULL THEN NAME
        ELSE
            'No name'
        END AS NAME
    ,   SEX_UPON_INTAKE
FROM 
    ANIMAL_INS
ORDER BY
    ANIMAL_ID ASC
```