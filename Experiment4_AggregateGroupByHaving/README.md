# Experiment 4: Aggregate Functions, Group By and Having Clause

## AIM
To study and implement aggregate functions, GROUP BY, and HAVING clause with suitable examples.

## THEORY

### Aggregate Functions 
These perform calculations on a set of values and return a single value.

- **MIN()** – Smallest value  
- **MAX()** – Largest value  
- **COUNT()** – Number of rows  
- **SUM()** – Total of values  
- **AVG()** – Average of values

**Syntax:**
```sql
SELECT AGG_FUNC(column_name) FROM table_name WHERE condition;
```
### GROUP BY
Groups records with the same values in specified columns.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name;
```
### HAVING
Filters the grouped records based on aggregate conditions.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

**Question 1**
--
<img width="1213" height="576" alt="Screenshot 2025-10-31 105152" src="https://github.com/user-attachments/assets/61218741-0fa9-424e-babb-a1338c6d3918" />


```sql
select Specialty,Gender,COUNT(*) as TotalDoctors
from Doctors
group by Specialty,Gender;
```

**Output:**

<img width="1231" height="693" alt="Screenshot 2025-10-31 105210" src="https://github.com/user-attachments/assets/21b9f9cc-7bb3-4d7c-b833-79033eb39431" />


**Question 2**
---
<img width="1212" height="600" alt="Screenshot 2025-10-31 105550" src="https://github.com/user-attachments/assets/86c8ce4f-592d-4c55-8a5c-2249e832b0c6" />


```sql
select Specialty,COUNT(*) as TotalDocto
from Doctors
