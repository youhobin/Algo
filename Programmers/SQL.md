### Select

---

#### 1. 평균 일일 대여 요금 구하기

round 반올림, as로 컬럼 이름 변경. 
```
SELECT ROUND(AVG(DAILY_FEE), 0) AS AVERAGE_FEE
From CAR_RENTAL_COMPANY_CAR 
WHERE CAR_TYPE = "SUV"
```

---
