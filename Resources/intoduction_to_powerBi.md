# Introduction to Power BI


### 1. What is Power BI, and how does it fit into the broader business intelligence landscape?

Power BI is a business intelligence (BI) tool developed by Microsoft that helps organizations transform raw data into meaningful insights through interactive reports and dashboards. It enables users to visualize data, perform analytics, and make data-driven decisions. Power BI integrates with various data sources, including Excel, databases, and cloud services, and offers AI-powered analytics to enhance decision-making.

### 2. What are the key components of Power BI, and what role does each play?

- **Power BI Desktop** – Windows application for creating reports and dashboards.  
- **Power BI Service (Cloud)** – Platform for publishing, sharing, and collaborating on reports.  
- **Power BI Mobile** – Access to reports and dashboards on mobile devices.  
- **Power BI Gateway** – Bridges on-premises data sources with the Power BI service.  
- **Power BI Report Server** – On-premises report hosting for enterprises with local data storage needs.

### 3. How does Power BI differ from other BI tools like Tableau and Google Data Studio?

| Feature | Power BI | Tableau | Google Data Studio |
|--------|----------|---------|--------------------|
| Ecosystem | Deep integration with Microsoft tools | Known for powerful visuals | Native to Google Cloud |
| Pricing | Cost-effective, scalable | Expensive for enterprises | Free |
| Use Case | General enterprise analytics | Advanced data exploration | Marketing & web analytics |

### 4. What are the different versions of Power BI?

- **Power BI Free** – Individual use with limited sharing.  
- **Power BI Pro** – Full collaboration and sharing features.  
- **Power BI Premium** – Dedicated capacity and enterprise-scale capabilities.  
- **Power BI Report Server** – On-premises report server for local deployment.

### 5. What are the different Power BI licensing options, and how do they impact usage?

- **Power BI Free** – No sharing or collaboration.  
- **Power BI Pro** – Enables report sharing, collaboration, and advanced features.  
- **Power BI Premium (Per User / Per Capacity)** – Enterprise features, large models, paginated reports.  
- **Power BI Embedded** – Embed reports in custom apps without end-user licenses.

### 6. What is Power BI Tenant Settings, and how does it impact governance?

Tenant settings, managed through the **Admin Portal**, allow administrators to control:

- Data export and sharing permissions  
- AI features and capacity usage  
- User roles for publishing and embedding  
- Security, compliance, and audit policies

### 7. What is the difference between Power BI Service Capacity and Power BI Premium Per User (PPU)?

| Feature | Power BI Service Capacity | Power BI Premium Per User (PPU) |
|---------|---------------------------|----------------------------------|
| Pricing | Based on capacity | Based on per-user licensing |
| AI Features | Yes | Yes |
| Paginated Reports | Yes | Yes |
| Deployment | Organization-wide | Individual users |

### 8. What is the difference between Power BI Free, Pro, and Premium licenses?

| Feature | Free | Pro | Premium |
|--------|------|-----|---------|
| Sharing | ❌ | ✅ | ✅ (Enterprise-wide) |
| AI & Paginated Reports | ❌ | Limited | ✅ |
| Data Capacity | 1 GB/user | 10 GB/user | Large models |
| On-Prem Report Server | ❌ | ❌ | ✅ |

### 9. What are the data sources supported by Power BI?

- SQL Server, MySQL, Oracle, PostgreSQL  
- Azure, AWS, Google Cloud, Salesforce  
- Excel, CSV, JSON, XML  
- APIs and Web sources  
- Microsoft apps like SharePoint, Dynamics 365, PowerApps

### 10. What are DAX and M in Power BI?

- **DAX (Data Analysis Expressions)** – Used for data modeling and calculations.  
- **M (Power Query Formula Language)** – Used in Power Query for transforming data before loading.

### 11. How does Power BI ensure data security and compliance?

- **Row-Level Security (RLS)**  
- **Azure Active Directory (AAD)** authentication  
- **Data encryption** (in transit and at rest)  
- **Compliance** with GDPR, HIPAA, SOC 2, and more

### 12. What are Power BI Dataflows?

Power BI Dataflows are cloud-based ETL solutions that enable reusable data transformation logic and centralized data preparation for multiple reports and datasets.

### 13. What is DirectQuery, and when should it be used?

**DirectQuery** allows live connections to data sources without importing. Ideal when:

- Datasets are too large for in-memory storage  
- Real-time analytics are needed  
- Data governance requires source-only storage

### 14. What is Composite Modeling in Power BI?

Composite Modeling enables combining **Import** and **DirectQuery** data sources in a single dataset, offering flexibility in balancing performance and data freshness.

### 15. How can Power BI be integrated with Python and R for advanced analytics?

Power BI supports executing Python and R scripts for:

- Data transformation  
- Machine learning models  
- Custom visualizations

### 16. What is Incremental Refresh in Power BI?

Incremental Refresh improves performance by refreshing only new or changed data, rather than the entire dataset, which is ideal for large or historical datasets.

### 17. What are Bookmarks in Power BI?

**Bookmarks** capture the current state of visuals, filters, and selections. They are used for:

- Storytelling  
- Navigation  
- Interactive report presentations

### 18. What is the role of Power BI Embedded?

Power BI Embedded allows developers to embed reports into web applications, giving external users access to BI insights without needing Power BI accounts.

### 19. What is the difference between Power Query and Power Pivot?

- **Power Query** – For data extraction, cleaning, and transformation (ETL).  
- **Power Pivot** – For data modeling, relationships, and DAX-based calculations.

### 20. What are the different types of Power BI visualizations?

Power BI supports various visual types, including:

- **Standard visuals**: Bar, Line, Pie, Map, Table, Matrix  
- **KPIs & Gauges**  
- **Custom visuals**: Available from Microsoft AppSource
