# limit, rownum

# 1.  MySql
limit 을 사용합니다.

```sql
SELECT
    *
FROM 
    PERSON
limit 1
```

# 2. Oracle
rownum을 사용합니다.

```sql
SELECT
    *
FROM 
    PERSON
WHERE
    ROWNUM <= 1
```