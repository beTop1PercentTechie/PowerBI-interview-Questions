### 21. What types of data sources can Power BI connect to?  
**Answer.** Power BI supports a wide range of data sources, including:  
- **Databases**: SQL Server, Oracle, MySQL, PostgreSQL, etc.  
- **Cloud Platforms**: Azure, Google BigQuery, AWS, etc.  
- **Online Services**: SharePoint, Salesforce, Google Analytics, etc.  
- **Local Files**: Excel, CSV, JSON, XML, etc.  
- **Web & APIs**: REST APIs, OData feeds, and web pages.

---

### 22. What is Power BI Embedded, and how can developers use it?  
**Answer.** Power BI Embedded is an Azure-based service that allows developers to integrate rich, interactive reports and dashboards into their web or mobile applications.  

Key highlights include:  
- **REST APIs & JavaScript SDK**: Embed and manage content programmatically.  
- **Custom Branding**: Supports white-labeling and role-based access.  
- **Scalability**: Designed for high-volume apps like SaaS platforms.  
- **Database Integration**: Connects to Azure SQL, Synapse, and on-premises sources.

---

### 23. How does Power BI integrate with Azure Synapse Analytics for big data processing?  
**Answer.** Power BI works seamlessly with Azure Synapse to deliver large-scale analytics:  
- **DirectQuery & Import**: Real-time querying and cached data support.  
- **Distributed Querying**: Leverages Synapse’s compute power for fast results.  
- **ETL Pipelines**: Uses Synapse pipelines for transforming and cleaning data.  
- **Security**: Integrated with Azure AD for identity and access control.  
- **ML Integration**: Utilize built-in ML models from Synapse in Power BI visuals.

---

### 24. What is a Power BI Data Gateway, and when should it be used?  
**Answer.** The Power BI Data Gateway bridges on-premises data with Power BI Service.  

Types of gateways:  
- **Standard Mode**: For enterprise-wide use.  
- **Personal Mode**: For individual users.  

**Use Cases**:  
The gateway is required when connecting Power BI Service to on-premises data like SQL Server, Oracle, or SAP that is not internet-facing.

---
### 25. How does Power BI handle unstructured data (e.g., JSON, XML)?  
**Answer.** Power BI can handle unstructured data using Power Query.

For **JSON** files, use
```m
Json.Document(File.Contents("filePath.json"))
```
For **XML** files, use
```m
Xml.Tables(File.Contents("filePath.xml"))
```
---
### 26. What is the difference between Dataflows and Linked Tables in Power BI?  
**Answer.**  
**Dataflows:**  
- Reusable ETL pipelines stored in Azure Data Lake.  
- Ideal for centralized data prep across multiple datasets.  

**Linked Tables:**  
- Referenced tables from existing datasets.  
- Reduces duplication and ensures data consistency.  

---

### 27. How does Power BI integrate with SAP HANA?  
**Answer.**  
- **DirectQuery Mode:** Enables live connectivity with real-time dashboards.  
- **SAP BW Connector:** Accesses structured data with hierarchies.  
- **Custom Queries:** Optimize performance via custom SQL.  
- **Security:** Supports SAP SSO and RBAC for data governance.  

---

### 28. What is the purpose of Power BI Deployment Pipelines?  
**Answer.**  
Deployment Pipelines manage report lifecycles across environments: **Dev → Test → Production**  
- Streamlines version control and testing.  
- Reduces errors through automation.  
- Supports incremental deployment for performance efficiency.  

---

### 29. What is Microsoft Fabric in Power BI?  
**Answer.**  
Microsoft Fabric is a unified platform that connects Power BI with data engineering, data science, and real-time analytics.  
- Built on OneLake storage for consistency.  
- Integrates with Azure Synapse, Data Factory, and ML models.  
- Supports real-time analytics, governance, and collaboration.  

---

### 30. How do you dynamically change measures in Power BI using a slicer?  
**Answer.**  
Use a disconnected table containing measure names and a `SWITCH()` function to update visuals based on user selection.

```dax
Selected Measure =
SWITCH(
    SELECTEDVALUE(MeasureList[MeasureName]),
    "Revenue", SUM(Sales[Revenue]),
    "Profit", SUM(Sales[Profit])
)
```
---

### 31. How does Power BI support AI-driven analytics?  
**Answer.**  
- **AI Visuals:** Key Influencers, Decomposition Tree.  
- **Azure ML Integration:** Consume ML models inside Power BI.  
- **AutoML:** Train predictive models directly in the Power BI Service.  

---

### 32. How do you implement time zone conversions in Power BI?  
**Answer.**  
- Store time zone offsets in a reference table.  
- Use DAX functions like `CONVERT()` or `SWITCH()` to adjust UTC timestamps.  
- Dynamically adjust based on user location or slicer input.  

---

### 33. How does Power BI integrate with SharePoint?  
**Answer.**  
- **Embed Reports:** Directly into SharePoint Online pages.  
- **Connect to Lists:** Use SharePoint Lists as data sources.  
- **Automation:** Combine with Power Automate for workflow integration.  

---

### 34. What is an XMLA Endpoint in Power BI, and how is it used?  
**Answer.**  
- Provides access to datasets via Analysis Services protocol.  
- Enables external tools like SSMS, DAX Studio, and Tabular Editor to query and modify models.  
- Available in Power BI Premium and Premium per User (PPU).  

---

### 35. How do you create a live connection to an SSAS model in Power BI?  
**Answer.**  
- Choose **Get Data > Analysis Services**.  
- Select **Live Connection** instead of Import.  
- Connect to a tabular or multidimensional model for real-time access.  

---

### 36. What is Synapse Link and how does it benefit Power BI?  
**Answer.**  
- Synapse Link connects Power BI directly to Azure Synapse Analytics.  
- Enables access to operational and transactional data in near real-time.  
- Eliminates the need for ETL pipelines, improving freshness and performance.  

---

### 37. How can you optimize Power BI report performance?  
**Answer.**  
- Use **Import Mode** for speed over DirectQuery when real-time isn't needed.  
- Enable **Aggregations** for pre-calculated metrics.  
- Apply **Incremental Refresh** for large datasets.  
- Avoid excessive **calculated columns** or complex visuals.  

---

### 38. What is Role-Level Security (RLS) and how is it implemented?  
**Answer.**  
- Restricts data access based on user roles.  
- Define **DAX filters** in the model for each role.  
- Assign roles in **Power BI Service > Dataset Settings**.  

---

### 39. How does Power BI connect with Azure Databricks?  
**Answer.**  
- Uses **Azure Databricks Connector** for high-scale analytics.  
- Supports **DirectQuery** and **Import** modes.  
- Allows **ML model output** to be visualized in Power BI dashboards.  

---

### 40. What are Aggregations in Power BI and how do they improve performance?  
**Answer.**  
- Aggregations summarize data at a higher level.  
- Improve performance by reducing the volume of data scanned.  
- Can be **manually** or **automatically managed**.  
- Ideal for large **fact tables** in enterprise models.  

---





