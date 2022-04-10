# datetime에서 시간 추출

# 1.  MySql
`HOUR`함수를 사용해서 추출합니다.
```sql
HOUR(DATETIME)
```

# 2. Oracle
`EXTRACT`와 `CAST`을 사용합니다.

```sql
EXTRACT(HOUR FROM CAST(DATETIME AS TIMESTAMP)) AS HOUR
```