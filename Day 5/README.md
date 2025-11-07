# 📅 Day 5 (07/11): Aggregate Functions — Summarizing Data Smartly  

Dived deep into SQL’s **aggregate functions** — the building blocks for any data analyst! 📊  

---

## 🔹 Functions Covered

- `COUNT()`  
- `SUM()`  
- `AVG()`  
- `MIN()`  
- `MAX()`  

---

## 🔹 Key Learnings

- Difference between `COUNT(*)` and `COUNT(column)`  
- How `AVG()` and `SUM()` handle `NULL` values  
- Use `ROUND()` for cleaner and more readable averages  
- Apply `DISTINCT` inside aggregates for unique counts  
- Always **alias** aggregates for better clarity and readability  

---

## 💡 Pro Tip  

> Aggregate functions **ignore NULL values** — use `COUNT(*)` if you want to include them in your calculations.  

---

## 🧠 Day 5 Challenge  

**Question:**  
Calculate the **total number of patients admitted**, **total patients refused**, and the **average patient satisfaction** across all services and weeks (rounded to 2 decimal places).  

```sql
SELECT 
    SUM(patients_admitted) AS patients_admitted,
    SUM(patients_refused) AS patients_refused,
    ROUND(AVG(patient_satisfaction), 2) AS satisfaction_score
FROM services_weekly;
