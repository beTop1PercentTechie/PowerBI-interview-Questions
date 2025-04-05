### 55. What is a data model in Power BI, and why is it important?  
**Answer.**  
A data model in Power BI is a structured framework that defines how data tables relate to each other through relationships. It enables efficient querying, accurate DAX calculations, and responsive visualizations by optimizing data organization and minimizing redundancy.

---

### 56. How do relationships work in Power BI, and what types can be created?  
**Answer.**  
Relationships in Power BI link tables through common columns to allow cross-table analysis. Types include:  
- **One-to-One (1:1):** One row in a table corresponds to one row in another  
- **One-to-Many (1:M):** One row in a primary table maps to multiple rows in a related table  
- **Many-to-Many (M:M):** Used when both tables have repeating values; often resolved via a bridge table  

---

### 57. What is a Star Schema, and why is it commonly used in Power BI?  
**Answer.**  
A Star Schema organizes data into a central fact table surrounded by dimension tables. It's preferred in Power BI for its simplicity, performance benefits, and ease of writing DAX expressions due to fewer and clearer relationships.

---

### 58. What is the difference between calculated columns and measures in Power BI?  
**Answer.**  
- **Calculated Columns:** Evaluated row-by-row and stored in the model. Used for static values (e.g., full names).  
- **Measures:** Evaluated at query time and used for dynamic aggregation (e.g., total sales). More memory-efficient than columns.  

---

### 59. How do calculated columns, measures, and calculated tables differ in Power BI?  
**Answer.**  
- **Calculated Columns:** Static, row-level computations stored in the table  
- **Measures:** Dynamic calculations evaluated at runtime based on user interaction  
- **Calculated Tables:** Entire tables generated from DAX expressions for custom aggregates or views  

---

### 60. How does a calculated table differ from a regular (imported) table in Power BI?  
**Answer.**  
A calculated table is created using DAX expressions within Power BI, while a regular table is imported from external sources. Calculated tables are useful for advanced modeling scenarios like role-playing dimensions or summary tables.

---

### 61. How can many-to-many relationships be handled in Power BI?  
**Answer.**  
- Use a bridge table with unique values  
- Apply `CROSSFILTER()` with bidirectional filtering carefully  
- Ensure proper granularity and filter direction to avoid ambiguity  

---

### 62. How do you manage relationships when working with unstructured or semi-structured data sources?  
**Answer.**  
- Clean and normalize data using Power Query  
- Create lookup tables for mapping  
- Use DAX functions like `RELATED()` and `TREATAS()` to simulate relationships  

---

### 63. How can referential integrity be ensured in Power BI models?  
**Answer.**  
- Use INNER JOINs in Power Query to exclude orphan records  
- Apply `ISBLANK()` in DAX to identify missing references  
- Use Data Profiling tools to validate consistency  

---

### 64. What are the different types of filters in Power BI, and how are they applied?  
**Answer.**  
- **Visual-Level Filters:** Apply to individual visuals  
- **Page-Level Filters:** Apply to all visuals on a page  
- **Report-Level Filters:** Apply across the entire report  
- **Drillthrough Filters:** Context-based filters for navigating between pages  

---

### 65. What are the different data storage modes in Power BI?  
**Answer.**  
- **Import Mode:** Data is loaded into memory (VertiPaq) for high performance  
- **DirectQuery Mode:** Data is queried in real-time from the source  
- **Dual Mode:** Hybrid of Import and DirectQuery for optimized performance  

---

### 66. What are Dataflows in Power BI, and when should they be used?  
**Answer.**  
Dataflows are cloud-based ETL features in the Power BI Service. They offer:  
- Reusable data preparation logic  
- Centralized transformation layer  
- Efficient handling of large/complex data  

---

### 67. How does Power BI Premium differ from Power BI Embedded?  
**Answer.**  
| Feature     | Power BI Premium     | Power BI Embedded        |
|------------|----------------------|---------------------------|
| Users      | Internal (Employees) | External (Customers)      |
| Licensing  | Per user or capacity | Pay-as-you-go via Azure   |
| Embedding  | Limited customization| Fully customizable        |

---

### 68. What are inactive relationships in Power BI, and when would you use them?  
**Answer.**  
Inactive relationships exist in the model but aren’t used unless activated via `USERELATIONSHIP()` in DAX. Useful when you have multiple relationships between two tables, e.g., Order Date vs. Ship Date.

---

### 69. What is row-level security (RLS) in Power BI and how is it implemented?  
**Answer.**  
RLS restricts data access by user role:  
- Define roles and filters using DAX  
- Assign users to roles in Power BI Service  
This ensures users only see data relevant to their role.

---

### 70. How do you optimize a Power BI data model for performance?  
**Answer.**  
- Remove unused columns and tables  
- Use star schema instead of snowflake  
- Minimize calculated columns  
- Leverage summary tables  
- Avoid high-cardinality columns in visuals  

---

### 71. What is the role of surrogate keys in Power BI modeling?  
**Answer.**  
Surrogate keys are artificial identifiers that simplify relationships and improve performance. They allow consistent joining across datasets, especially when natural keys are inconsistent or missing.

---

### 72. How can circular dependency errors in Power BI be resolved?  
**Answer.**  
- Avoid calculated columns/tables that refer to each other  
- Break logic into smaller, independent pieces  
- Replace columns with measures if possible  
- Redesign the model for clearer dependencies  

---

### 73. What is a composite model in Power BI?  
**Answer.**  
A composite model combines multiple sources with different storage modes (Import + DirectQuery). It allows flexible, scalable models while maintaining performance and enabling real-time data when needed.

---

### 74. How can you create role-playing dimensions in Power BI?  
**Answer.**  
- Create multiple relationships to the same dimension (e.g., Order Date, Ship Date)  
- Keep one relationship active  
- Use `USERELATIONSHIP()` in DAX to switch context for inactive relationships

---
