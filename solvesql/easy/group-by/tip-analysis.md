# 1. 설명
DAY, TIME - GROUP BY
DAY, TIME - 오름 차순
TIP 평균 소수점 3번째 반올림
SIZE 평균 소수점 3번째 반올림

[문제 링크](https://solvesql.com/problems/tip-analysis/)


# 2. 코드
### 1) SQLite
```sql
SELECT
    DAY
  , TIME
  , ROUND(AVG(TIP), 2) AVG_TIP
  , ROUND(AVG(SIZE), 2) AVG_SIZE
FROM
  TIPS
GROUP BY
    DAY
  , TIME
ORDER BY
    DAY ASC
  , TIME ASC
```
