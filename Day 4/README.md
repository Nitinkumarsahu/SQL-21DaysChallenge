# 📅 Day 4 (06/11): LIMIT & OFFSET — The Art of Pagination  

Today’s focus was on managing query results efficiently with **LIMIT** and **OFFSET**.  
Learned how to paginate through data like a pro! 🚀  

---

## 🔹 Key Concepts

- **LIMIT** restricts the number of rows returned  
- **OFFSET** skips a specified number of rows before returning results  
- **Pagination formula:**  
- **Always combine `ORDER BY` with `LIMIT`** for consistent and predictable results  

---

## 💡 Pro Tip

> Test queries with **LIMIT** before running them on large datasets to avoid unnecessary load on the database.

---

## 🧠 Day 4 Challenge

**Question:**  
Fetch the **3rd to 7th highest patient satisfaction scores** from the `patients` table, showing:  

- `patient_id`  
- `name`  
- `service`  
- `satisfaction`  

```sql

SELECT patient_id, name, service, satisfaction
FROM patients
ORDER BY satisfaction DESC
LIMIT 5 OFFSET 2;
