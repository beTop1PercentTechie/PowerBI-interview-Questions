### 305. How does Power BI handle real-time data streaming?  
**Answer:**  
Power BI enables real-time data streaming through three primary mechanisms:  
- **Push Datasets:** Data is pushed into Power BI via REST API, allowing for near real-time dashboard updates.  
- **Streaming Datasets:** Ideal for IoT scenarios, data is ingested through continuous streams from sources like sensors or telemetry APIs.  
- **Azure Stream Analytics:** This service can process real-time data and output it directly to Power BI dashboards for live monitoring.  

---

### 306. What are the key differences between Push, Streaming, and Hybrid datasets in Power BI?  
**Answer:**  
- **Push Dataset:** Data is pushed periodically via the Power BI REST API. The data is stored and supports report creation using the tabular model.  
- **Streaming Dataset:** Data flows in real-time but is not stored—ideal for live visuals only (e.g., line charts, cards).  
- **Hybrid Dataset:** Combines push and streaming capabilities. It streams data while also storing it for historical analysis and richer visualizations.  

---

### 307. How does a Dataflow differ from a Shared Dataset in Power BI?  
**Answer:**  
| Feature     | Dataflow                         | Shared Dataset                      |  
|------------|----------------------------------|-------------------------------------|  
| Purpose     | Reusable ETL logic and data prep | Reusable semantic/report model      |  
| Storage     | Azure Data Lake Gen2             | Power BI Service (in-memory)        |  
| Processing  | Power Query (in cloud)           | Tabular engine (in Power BI)        |  

---

### 308. How do you build real-time dashboards in Power BI?  
**Answer:**  
To build real-time dashboards:  
- Create a Streaming or Push Dataset using REST APIs or streaming endpoints.  
- Use tools like Azure Stream Analytics, Power Automate, or custom applications to feed data.  
- Use tiles like line charts, cards, and gauges which support live visuals.  
- Pin visuals to a dashboard, not just a report, to enable real-time rendering.  

---

### 309. How can you integrate Power BI with IoT devices and data sources?  
**Answer:**  
- Use Azure IoT Hub to collect data from IoT devices.  
- Stream this data into Azure Stream Analytics, where it can be transformed and pushed into Power BI.  
- Set up Streaming Datasets or connect using Power BI REST API to visualize real-time telemetry like temperature, device uptime, or motion detection.  

---

### 310. What are Streaming Dataflows in Power BI?  
**Answer:**  
Streaming Dataflows allow ingestion and transformation of real-time data using Power Query Online. These are especially useful when you want to preprocess streaming data (like filtering or transformation) before it reaches a dataset or dashboard. This combines the flexibility of Power Query with real-time ingestion.  

---

### 311. What types of visuals support real-time updates in Power BI dashboards?  
**Answer:**  
Real-time dashboards support a subset of visuals:  
- Cards and KPIs  
- Line and Clustered Column Charts  
- Gauge Visuals  
- Custom visuals that support streaming  
These visuals can auto-refresh with streaming data for live updates.  

---

### 312. Can you apply data transformation or DAX measures on Streaming Datasets?  
**Answer:**  
Streaming Datasets do not support data transformations or DAX because data is not stored in a model. If you need such functionality, use Push Datasets or Hybrid Datasets to persist data and enable modeling features.  

---

### 313. What limitations exist when working with real-time data in Power BI?  
**Answer:**  
- Streaming datasets do not support complex visuals or DAX calculations.  
- There is a 1 million rows/day limit on data ingestion for push datasets (can vary by licensing).  
- Data retention in pure streaming datasets is temporary (typically ~60 minutes).  
- Dashboard tiles refresh in real-time, but report visuals do not auto-refresh.  

---

### 314. What role does Azure Stream Analytics play in Power BI real-time solutions?  
**Answer:**  
Azure Stream Analytics acts as a real-time data processing engine that can:  
- Ingest high-velocity data from sources like IoT Hub or Event Hub  
- Perform SQL-like transformations on the data  
- Output directly to Power BI to power live dashboards  
This makes it a vital connector between data producers and Power BI.  

---

### 315. How does Power BI Embedded handle real-time data scenarios?  
**Answer:**  
Power BI Embedded can show real-time dashboards and visuals by embedding live reports into web applications. When used with Push or Streaming Datasets, the visuals update dynamically. Developers can use JavaScript API to refresh visuals or trigger interactions programmatically.  

---

### 316. How do you monitor device health and performance using Power BI in an industrial IoT scenario?  
**Answer:**  
- Collect telemetry data from devices using IoT Hub or MQTT brokers.  
- Process this data with Stream Analytics for filtering and aggregation.  
- Push the processed data into Power BI for real-time monitoring of device metrics like CPU usage, temperature, or alert conditions.  
- Use alerts and Power Automate for automated response to anomalies.  

---

### 317. Can Power BI trigger alerts from real-time dashboards?  
**Answer:**  
Yes. Power BI supports data-driven alerts for dashboard tiles using push or streaming datasets. When a value crosses a specified threshold (e.g., temperature > 80°C), Power BI can send emails or trigger a Power Automate flow.  

---

### 318. What is the best practice for historical analysis of streaming data in Power BI?  
**Answer:**  
Since streaming datasets are transient, best practice involves:  
- Using Azure Data Lake or Azure SQL for storing raw telemetry data.  
- Using Power BI Dataflows or DirectQuery for historical trend analysis.  
- Combine with real-time streaming for unified dashboards that support both instant and long-term insights.  

---

### 319. Is it possible to refresh a streaming dataset manually?  
**Answer:**  
No. Streaming datasets do not support manual or scheduled refresh since data is continuously fed into Power BI. Push and Hybrid datasets, however, can be refreshed or updated via API.  

---

### 320. How do Power BI and Power Automate work together in real-time monitoring scenarios?  
**Answer:**  
Power Automate can be used to:  
- Trigger flows when alerts are activated on Power BI dashboards.  
- Push new data into Power BI using the "Add Rows to Dataset" action.  
- Notify stakeholders or update logs when real-time thresholds are breached.  

---
