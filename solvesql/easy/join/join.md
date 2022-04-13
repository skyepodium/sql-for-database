# 1. 설명
Golf 종목에 참여한 선수들의 id를 조회하세요

[문제 링크](https://solvesql.com/problems/join/)


# 2. 코드
### 1) SQLite
```sql
SELECT
  DISTINCT ATHLETE_ID
FROM
  EVENTS E
    INNER JOIN 
  RECORDS R 
    ON E.ID = R.EVENT_ID
    AND E.SPORT = 'Golf'
```
