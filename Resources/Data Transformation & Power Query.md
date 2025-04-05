### 41. How does Power Query assist in data transformation?  
**Answer:**  
Power Query is a powerful data transformation engine in Power BI that enables users to clean, reshape, and prepare data before loading it into the data model.  
Common transformation steps include:  
- Removing duplicates  
- Changing data types  
- Merging and appending queries  
- Splitting and combining columns  
- Pivoting and unpivoting data  

---

### 42. What is the role of the M language in Power Query, and how is it different from DAX?  
**Answer:**  
- **M Language:** A functional language used during the data loading phase for defining complex data transformations.  
- **DAX:** Used post-loading for calculations like measures, calculated columns, and custom aggregations.  
M is used in Power Query, while DAX is used in the data model.

---

### 43. What is Query Folding, and why is it important in Power BI?  
**Answer:**  
Query Folding refers to the process where Power Query translates transformations into native source queries.  
Benefits include:  
- Improved performance  
- Reduced memory usage  
- Faster data refresh times  

---

### 44. What’s the difference between merging and appending queries in Power BI?  
**Answer:**  
- **Merge Queries:** Combines columns from two tables using a join logic (like SQL JOIN).  
- **Append Queries:** Stacks rows from two or more tables vertically (like SQL UNION).  

---

### 45. How does Data Profiling in Power Query help during data cleaning?  
**Answer:**  
Data Profiling provides insights into data structure and quality:  
- Missing or null values  
- Unique and duplicate entries  
- Column value distribution  
Helps identify issues early for effective cleaning.

---

### 46. How can Power Query transformations be optimized for large datasets?  
**Answer:**  
- Leverage query folding wherever possible  
- Reduce data early (remove unused columns and rows)  
- Use staging queries for modular logic  
- Minimize applied steps  

---

### 47. How does Power BI support multi-language reporting?  
**Answer:**  
- **Translation Tables:** Use locale-specific labels  
- **DAX Logic:** `SWITCH()` with `USERPRINCIPALNAME()`  
- **Power BI Service:** Locale settings render appropriate language views  

---

### 48. What is Query Folding in Power Query, and why is it beneficial?  
**Answer:**  
Query Folding pushes transformation logic back to the source system.  
Benefits:  
- Optimized refresh performance  
- Reduced local resource usage  
- Scales better for enterprise data models  

---

### 49. How can you check if Query Folding is happening in Power Query?  
**Answer:**  
- Right-click any applied step in Power Query Editor  
- Select **View Native Query**  
- If enabled, query folding is active; if disabled, folding is broken  

---

### 50. What are some best practices for writing M code in Power Query?  
**Answer:**  
- Minimize and consolidate steps  
- Use clear variable names with `let` and `in`  
- Remove unnecessary columns early  
- Favor folding-compatible transformations  

---

### 51. How do you create a reusable custom function in M?  
**Answer:**  
You can define a function using `let` and the `=>` operator:  
```m
let  
    myFunction = (x as number) => x * 2  
in  
    myFunction
```
---

### 52. What is the role of Data Profiling in Power Query?  
**Answer:**  
Data Profiling provides a visual analysis of column-level statistics such as:  
- Value distribution  
- Null values  
- Min/Max values  
- Distinct and duplicate count  

This helps ensure data quality before it is loaded into the Power BI data model.

---

### 53. What types of joins are supported in Power Query?  
**Answer:**  
Power Query supports the following join types:  
- **Inner Join** – Returns matching rows from both tables  
- **Left Outer Join** – All rows from the left table, plus matching rows from the right  
- **Right Outer Join** – All rows from the right table, plus matching rows from the left  
- **Full Outer Join** – All rows from both tables  
- **Left Anti Join** – Rows from the left table with no match in the right  
- **Right Anti Join** – Rows from the right table with no match in the left  

---

### 54. Why is Query Folding crucial in enterprise-grade data models?  
**Answer:**  
Query Folding is critical because it:  
- Offloads processing to efficient server engines (e.g., SQL Server)  
- Reduces memory and CPU usage on local machines  
- Improves refresh performance and enables scalable data models in enterprise environments  

---
