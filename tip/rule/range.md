# 0 ~ 23 출력하기

# 1. MySql
```sql
WITH RECURSIVE cte AS (
    SELECT 0 AS n
    UNION ALL
    SELECT n + 1 FROM cte WHERE n < 23
)
SELECT 
    n as HOUR 
FROM 
    cte
```

# 2. Oracle
```sql
SELECT 
    ROWNUM - 1 as HOUR
FROM DUAL
CONNECT BY Rownum <= 24
```