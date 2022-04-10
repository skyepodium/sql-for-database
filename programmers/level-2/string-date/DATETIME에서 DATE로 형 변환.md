# 1. 설명
년, 월, 일만 보여주세요

[문제 링크](https://programmers.co.kr/learn/courses/30/lessons/59414)


# 2. 코드
### 1) MySql
```sql
SELECT
        ANIMAL_ID
    ,   NAME
    ,   DATE_FORMAT(DATETIME, '%Y-%m-%d') AS 날짜
FROM
    ANIMAL_INS
ORDER BY
    ANIMAL_ID ASC
```

### 2) Oracle
```sql
SELECT
        ANIMAL_ID
    ,   NAME
    ,   TO_CHAR(DATETIME, 'YYYY-MM-DD') AS 날짜
FROM
    ANIMAL_INS
ORDER BY
    ANIMAL_ID ASC
```