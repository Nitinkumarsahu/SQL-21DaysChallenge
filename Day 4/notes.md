# 📅 Day 4 — 21 Days IDC SQL Challenge  

## 🧠 Topic: SQL LIMIT, OFFSET, and ORDER BY  

### 🎯 Objective  
Learn how to:
- Retrieve a specific number of rows using **LIMIT**
- Skip rows using **OFFSET**
- Sort data using **ORDER BY**
- Combine these clauses to extract ranked or paginated results

---

## 🧩 Tasks and Solutions  

### 🩺 **1️⃣ Display the first 5 patients from the patients table**
```sql
SELECT * 
FROM patients
LIMIT 5;
```
### 🩺 **2️⃣ Show patients 11–20 using OFFSET
```sql
SELECT * 
FROM patients
LIMIT 10 OFFSET 10;
```
### 🩺 **3️⃣ Get the 10 most recent patient admissions based on arrival_date
```sql
SELECT * 
FROM patients
ORDER BY arrival_date DESC
LIMIT 10;
```
### 🩺 **4️⃣ Find the 3rd to 7th highest patient satisfaction scores
```sql
SELECT 
    patient_id,
    name,
    service,
    satisfaction
FROM patients
ORDER BY satisfaction DESC
LIMIT 5 OFFSET 2;
