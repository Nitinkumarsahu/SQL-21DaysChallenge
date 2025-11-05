# 🧠 Day 2 & Day 3 — 21 Days of SQL Challenge 🚀

## 📅 Day 2 — Aggregations, GROUP BY, WHERE vs HAVING

### 🧩 What I Learned
- Aggregate functions combine multiple rows into a single value using:
  - `COUNT`, `SUM`, `AVG`, `MIN`, `MAX`
- Practiced `GROUP BY` to roll up data by columns like **service** or **year**.
- Clarified the difference between `WHERE` and `HAVING`:
  - `WHERE` filters **rows before grouping**
  - `HAVING` filters **groups after aggregation**

### 💻 Problem
Find all patients admitted to the **Surgery** service with a satisfaction score below 70, showing their:
- `patient_id`
- `name`
- `age`
- `satisfaction score`

### 🧾 Query
```sql
SELECT patient_id, name, age, satisfaction
FROM patients
WHERE service = 'Surgery' AND satisfaction < 70;
```

# 📅 Day 3 — Sorting Data with ORDER BY 🚀

### 🧩 What I Learned
- Explored the basics of `ORDER BY` for sorting data.
- Learned about:
  - `ASC` (ascending, default)
  - `DESC` (descending)
  - Multi-column sorting for advanced ordering.
- Practiced **Top-N patterns** using `ORDER BY` with `LIMIT`.

---

### 💻 Problem Statement
Retrieve the **top 5 weeks** with the highest patient refusals across all services, displaying:

- `week`
- `service`
- `patients_refused`
- `patients_request`

Sort results by `patients_refused` in **descending order**.

---

### 🧾 SQL Query
```sql
SELECT week, service, patients_refused, patients_request
FROM services_weekly
ORDER BY patients_refused DESC
LIMIT 5;
