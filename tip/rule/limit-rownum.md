# limit, rownum

# 1.  MySql
limit 을 사용합니다.

```sql
SELECT 
    NAME
FROM 
    ANIMAL_INS
ORDER BY 
    DATETIME ASC
LIMIT 1
```

# 2. Oracle
전체 결과를 한번 감싼 후 `ROWNUM`으로 구분합니다.

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