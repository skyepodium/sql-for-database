# 1. 설명
홀수명이 방문한 테이블을 조회하세요

[문제 링크](https://solvesql.com/problems/size-of-table/)


# 2. 코드
### 1) SQLite
```sql
SELECT
  *
FROM
  TIPS
WHERE
  SIZE % 2 == 1
```
