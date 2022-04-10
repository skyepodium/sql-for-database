# 1. 설명
강아지이고 이름에 el이 들어가는 동물을 조회하세요

[문제 링크](https://programmers.co.kr/learn/courses/30/lessons/59047)


# 2. 코드
### 1) MySql
```sql
SELECT 
        ANIMAL_ID
    ,   NAME
FROM 
    ANIMAL_INS
WHERE 
    ANIMAL_TYPE = 'Dog' 
        AND 
    NAME LIKE '%el%'
ORDER BY 
    NAME ASC
```

### 2) Oracle
```sql
SELECT 
        ANIMAL_ID
    ,   NAME
FROM 
    ANIMAL_INS
WHERE 
    ANIMAL_TYPE = 'Dog' 
        AND 
    LOWER(NAME) LIKE '%el%'
ORDER BY 
    NAME ASC
```