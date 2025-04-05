### 137. What is DirectQuery in Power BI, and how does it differ from Import Mode?
**Answer:**  
DirectQuery enables real-time querying of the data source without importing data into Power BI. Unlike Import Mode, which loads data into memory for faster performance and offline access, DirectQuery sends queries live to the source upon interaction.

- **Import Mode**: Faster and suitable for high-performance reports; requires scheduled refreshes.  
- **DirectQuery**: Real-time data; may suffer slower performance due to dependency on source query time.

---

### 138. What are the key advantages and limitations of using DirectQuery in Power BI?
**Answer:**  
**Advantages:**
- Real-time analytics with up-to-date data.
- Efficient for large datasets that can't fit into memory.

**Limitations:**
- Slower performance due to live querying.
- Limited DAX and transformation capabilities.
- Dependency on source system’s availability and responsiveness.

---

### 139. What is Composite Model in Power BI, and how does it enhance data modeling?
**Answer:**  
Composite Models allow blending both Import and DirectQuery modes in a single dataset. This enables a hybrid approach—using Import for frequently queried data and DirectQuery for real-time needs—maximizing performance and flexibility.

---


### 140. How can you efficiently handle large datasets in Power BI?
**Answer:**  
- Use **Aggregations** for summary-level data.
- Design using a **Star Schema**.
- Apply **Incremental Refresh**.
- Prefer **DAX Measures** over calculated columns.
- Consider **DirectQuery** for volatile or large-scale datasets.
---
### 141. What is Incremental Refresh in Power BI, and why is it useful?
**Answer:**  
Incremental Refresh only updates new or modified data rather than the full dataset, drastically reducing refresh duration and improving scalability for large datasets.

---

### 142. What are Aggregations in Power BI, and how do they boost performance?
**Answer:**  
Aggregations are pre-summarized tables Power BI uses to resolve queries faster by avoiding full dataset scans. They help scale reports for large datasets by reducing runtime complexity.

---
### 143. How can you address memory limitations in the Power BI Service?
**Answer:**  
- Use **Aggregation tables**.  
- Implement **Incremental Refresh**.  
- Optimize data types and reduce high-cardinality columns.  
- Remove unused columns/tables.  
- Apply compression during load.
---
### 144. Why might a Power BI dataset refresh fail, and how do you troubleshoot it?
**Answer:**  
Common causes include:
- Invalid credentials.
- Gateway issues.
- Query timeouts.
- Source system errors.

**Troubleshooting :** Use the **refresh history and error logs** in the Power BI Service.

---
### 145. How does Power BI optimize large dataset performance?
**Answer:**  
Through:
- Aggregations  
- Incremental Refresh  
- Hybrid Tables  
- Efficient DAX coding  
- Proper star schema modeling

---

### 146. What is Query Folding in Power Query, and why is it important?
**Answer:**  
Query Folding is the translation of M transformations into native queries at the source. It boosts performance by pushing processing to the data source, reducing Power BI’s memory workload.

### 147. How do you create and reuse a custom function in M language (Power Query)?
**Answer:**
```m
let
    MultiplyByTwo = (x as number) => x * 2
in
    MultiplyByTwo
```
- This function can be called in other queries or columns by referencing it directly.
---
### 148. What are the different storage modes available in Power BI, and when should each be used?
**Answer:**  
- **Import Mode:** Best for performance and offline scenarios.  
- **DirectQuery Mode:** Best for real-time analytics and large datasets.  
- **Dual Mode:** Tables act as both Import and DirectQuery based on context, enabling modeling and performance flexibility.
---
### 149. What are Hybrid Tables in Power BI, and how do they help?
**Answer:**  
Hybrid Tables combine **Import Mode** for historical data and **DirectQuery** for real-time data in the same table. This enables high performance and up-to-date reporting in one model.
---
### 150. How can you improve Power Query performance during data transformations?
**Answer:**  
- Minimize applied steps.  
- Use `Table.Buffer()` for caching.  
- Preserve query folding.  
- Avoid row-by-row operations when possible.
---
### 151. How do you optimize Power BI reports built on large datasets?
**Answer:**  
- Use Aggregations and Incremental Refresh.  
- Reduce visuals and slicers.  
- Eliminate unused columns/relationships.  
- Optimize DAX using variables and avoid complex measures.
---
### 152. What is the difference between Calculated Columns and Measures in Power BI?
**Answer:**  
- **Calculated Columns:** Pre-calculated during data refresh; consume memory.  
- **Measures:** Calculated at runtime; preferred for performance and scalability.
---
### 153. What are Parameters in Power Query, and how are they useful?
**Answer:**  
Parameters are user-defined inputs used to dynamically filter or configure queries, enabling flexible and reusable transformations.

---
### 154. How does Power BI handle data refresh in DirectQuery mode?
**Answer:**  
In DirectQuery, data is not stored in memory. Queries are executed in real time (or via cache settings) whenever visuals are interacted with.

---
### 155. What are best practices for designing a Power BI data model for performance?
**Answer:**  
- Prefer **Star Schema**.  
- Avoid bi-directional relationships.  
- Reduce column cardinality.  
- Eliminate unused fields.  
- Use surrogate keys.
---
### 156. What is Dual Storage Mode, and how is it different from Composite Models?
**Answer:**  
- **Dual Mode:** A single table can act as Import or DirectQuery based on usage.  
- **Composite Models:** Use both Import and DirectQuery tables in the same dataset.
---
### 157. What is a Power BI Aggregation Table, and how is it different from a regular table?
**Answer:**  
Aggregation tables are **pre-summarized** fact tables that Power BI uses to speed up queries. They minimize scanning large datasets for repeated calculations.

---
### 158. How does the Star Schema improve Power BI performance?
**Answer:**  
- Simplifies relationships.  
- Improves aggregation efficiency.  
- Reduces query complexity.  
- Optimizes DAX performance with VertiPaq engine.
---
### 159. What is the role of the Storage Engine and Formula Engine in Power BI?
**Answer:**  
- **Storage Engine (SE):** Retrieves data via VertiPaq (Import) or SQL (DirectQuery).  
- **Formula Engine (FE):** Executes DAX and manages query context and logic.
---
### 160. How can you reduce dataset size in Power BI?
**Answer:**  
- Remove unused columns/tables.  
- Use efficient data types.  
- Lower cardinality.  
- Avoid calculated columns.  
- Filter unnecessary data in Power Query.
---
### 161. What is the role of the Power BI Performance Analyzer, and how do you use it?
**Answer:**  
It helps optimize report performance by logging:
- DAX query duration  
- Visual rendering time  
- Background tasks  

Use it to identify bottlenecks and improve performance.

---
### 162. What are best practices when using DirectQuery in production reports?
**Answer:**  
- Limit visuals per page.  
- Apply filters to reduce data load.  
- Avoid complex DAX.  
- Use source-side aggregations.  
- Use parameters to limit data scope.
---
### 163. What are limitations of using DirectQuery compared to Import Mode?
**Answer:**  
- Slower performance.  
- Limited time intelligence functions.  
- Source dependency and query limits (1 million rows).  
- Higher load on the source system.
---
### 164. What is a Buffered Table in Power Query, and when should you use it?
**Answer:**  
Use `Table.Buffer()` to cache results and prevent repeated evaluations. It ensures consistent performance when referencing the same table multiple times.

---
### 165. How can you identify whether a transformation in Power Query supports query folding?
**Answer:**  
Right-click a step and select **"View Native Query"**. If available, query folding is active. Grayed out means folding has been broken.

---
### 166. What is the purpose of defining data types in Power Query early in the query steps?
**Answer:**  
Setting data types early ensures accurate transformation behavior and helps Power Query apply optimized functions. It also supports query folding and reduces the risk of errors during refresh or DAX usage. Delaying type assignments can break folding and introduce inconsistencies.

---

