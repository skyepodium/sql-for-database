# 별칭

# 1. FROM
### 1)  MySql
`as` 키워드로 명시하거나 생략할 수 있습니다.
```sql
SELECT
        p.firstName
FROM 
    Person as p
        LEFT JOIN
    Address as a
        ON p.personId = a.personId
```

### 2) Oracle
from 절의 alias에는 `as` 키워드를 사용할 수 없습니다.

```sql
SELECT
        p.firstName
FROM 
    Person p
        LEFT JOIN
    Address a
        ON p.personId = a.personId
```

# 2. SELECT
### 1) Mysql
`'' 따옴표` 있을수도 있고 없을수도 있습니다.
```sql
SELECT
       CASE WHEN SEX_UPON_INTAKE LIKE '%Neutered%' OR SEX_UPON_INTAKE LIKE '%Spayed%'
        THEN 'O'
            ELSE 'X'
        END AS 중성화
FROM 
    ANIMAL_INS
```

### 2) Oracle
`'' 따옴표` 로 alias를 지정할 수 없습니다.
```sql
SELECT
       CASE WHEN SEX_UPON_INTAKE LIKE '%Neutered%' OR SEX_UPON_INTAKE LIKE '%Spayed%'
        THEN 'O'
            ELSE 'X'
        END AS 중성화
FROM 
    ANIMAL_INS
```