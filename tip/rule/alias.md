# 별칭

# 1.  MySql
as 키워드로 명시하거나 생략할 수 있습니다.
```sql
SELECT
        p.firstName
    ,   p.lastName
    ,   a.city
    ,   a.state
FROM 
    Person as p
        LEFT JOIN
    Address as a
        ON p.personId = a.personId
```

# 2. Oracle
from 절의 alias에는 `as` 키워드를 사용할 수 없습니다.

```sql
SELECT
        p.firstName
    ,   p.lastName
    ,   a.city
    ,   a.state
FROM 
    Person p
        LEFT JOIN
    Address a
        ON p.personId = a.personId
```