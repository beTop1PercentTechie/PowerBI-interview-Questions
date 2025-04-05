### 104. What types of visualizations are available in Power BI?  
**Answer:**  
Power BI offers a wide variety of built-in visualizations, including:  
- **Bar and Column Charts** – Great for comparing values across categories.  
- **Line and Area Charts** – Useful for trend analysis over time.  
- **Pie and Donut Charts** – Represent parts of a whole.  
- **Scatter and Bubble Charts** – Analyze relationships between numeric variables.  
- **Tables and Matrices** – Display detailed, tabular data.  
- **Maps (Basic and Shape Maps)** – Geospatial data visualization.  
- **Gauge and Card Visuals** – Showcase KPIs and summary metrics.  
- **Custom Visuals** – Imported from AppSource or developed using Power BI Visuals SDK.

---

### 105. What is the difference between slicers and filters in Power BI?  
**Answer:**  
Filters can be applied at different levels:  
- **Visual-level filters** – Affect a specific visual.  
- **Page-level filters** – Apply to all visuals on a page.  
- **Report-level filters** – Affect all pages in the report.  
Slicers are visual controls that allow users to interactively filter the data on a report page. They enhance user experience by offering an intuitive filtering mechanism.

---

### 106. What are drill-down, drill-through, and cross-filtering features in Power BI?  
**Answer:**  
- **Drill-down** allows users to explore data at different levels of granularity within the same visual hierarchy (e.g., Year → Quarter → Month).  
- **Drill-through** navigates users to a separate, detailed page based on a specific selection.  
- **Cross-filtering** enables interactivity between visuals—selecting a data point in one visual filters data in other visuals automatically.

---

### 107. How can custom visuals be created and used in Power BI?  
**Answer:**  
Custom visuals can be developed using the Power BI Visuals SDK and packaged as `.pbiviz` files. These visuals can also be:  
- Downloaded from Microsoft AppSource, or  
- Imported directly into Power BI Desktop via the **"Import from marketplace"** or **"Import a visual from file"** options.

---

### 108. What is the purpose of Deployment Pipelines in Power BI?  
**Answer:**  
Deployment Pipelines enable controlled movement of content across environments—**Development → Test → Production**. They offer:  
- Version control,  
- Environment-specific configuration, and  
- Improved collaboration during report lifecycle management.

---

### 109. What are the different types of filters available in Power BI?  
**Answer:**  
Power BI supports several filtering options:  
- Visual-level filters  
- Page-level filters  
- Report-level filters  
- Drillthrough filters  
- Top N filters  
- Relative date filters

---

### 110. How does cross-highlighting differ from cross-filtering in Power BI?  
**Answer:**  
- **Cross-highlighting** emphasizes related data points in other visuals while preserving the full dataset.  
- **Cross-filtering** changes the dataset in the related visuals based on selection, offering more granular control over interactivity.

---

### 111. What are tooltip pages in Power BI?  
**Answer:**  
Tooltip pages are dedicated report pages that appear as popups when a user hovers over a visual. These pages can contain rich and detailed visuals, offering context without cluttering the main report.

---

### 112. Can you explain bookmarks and how they enhance interactivity in Power BI?  
**Answer:**  
Bookmarks capture the current state of a report page—including filters, slicers, and visuals. They can be used for:  
- Creating interactive storytelling  
- Custom navigation  
- Simulating report features like tabbed layouts or dynamic views

---

### 113. What are KPI and Card visuals in Power BI, and when are they used?  
**Answer:**  
- **Card visuals** display a single number or measure (e.g., Total Sales).  
- **KPI visuals** compare a current value to a target (goal), showing trends and performance.  
These are typically used for dashboard-level summaries and high-level performance indicators.

---

### 114. How do themes enhance Power BI reports?  
**Answer:**  
Themes allow for consistent styling across visuals, including colors, fonts, and data labels. They can be customized via JSON files and imported into Power BI to align with branding or improve readability.

---

### 115. What is the Smart Narrative visual in Power BI?  
**Answer:**  
The Smart Narrative visual automatically generates natural language summaries of data insights and trends. It's particularly useful for storytelling or creating dynamic report descriptions without writing custom text.

---

### 116. How can you highlight specific data points dynamically in a Power BI visual?  
**Answer:**  
You can use DAX-based measures combined with conditional formatting to highlight specific values.  
Example: highlight values above a threshold or matching a slicer selection by changing color or font.

---

### 117. What are report tooltips, and how are they different from default tooltips in Power BI?  
**Answer:**  
- **Default tooltips** display basic information (like value, category) when hovering over a visual.  
- **Report tooltips** are custom-built report pages that offer richer content and greater design control.

---

### 118. How do you use conditional formatting in Power BI visuals?  
**Answer:**  
Conditional formatting allows dynamic changes to color, font, or data bars in visuals based on values or rules. Common in tables, matrices, and KPI visuals to draw attention to key data points.

---

### 119. What are small multiples in Power BI, and when should you use them?  
**Answer:**  
Small multiples split a visual into a grid of smaller visuals, each representing a category (e.g., region). Useful for comparing the same metric across different categories in a compact layout.

---

### 120. What is the difference between a matrix and a table visual in Power BI?  
**Answer:**  
- **Table** – Displays data in a flat, row-by-row format.  
- **Matrix** – Adds row and column groupings (like pivot tables), supporting drill-down and subtotals.

---

### 121. How can you implement dynamic titles or labels in Power BI visuals?  
**Answer:**  
Dynamic titles can be created using DAX measures that return text based on slicer or filter selections. These measures are inserted into visual titles using the **fx** option under the formatting pane.

---

### 122. What are the benefits of using a paginated report versus a Power BI interactive report?  
**Answer:**  
- **Paginated Reports** – Pixel-perfect, printable reports for formal needs (e.g., invoices).  
- **Power BI Reports** – Interactive dashboards ideal for exploration and real-time analysis.

---

### 123. How do you optimize visuals for performance in Power BI reports?  
**Answer:**  
Performance tips include:  
- Reducing the number of visuals per page  
- Avoiding complex DAX inside visuals  
- Using summarized tables  
- Limiting slicers and unnecessary custom visuals

---

### 124. How can you create a report that supports multiple languages in Power BI?  
**Answer:**  
Localization can be achieved using translation tables and a language selector slicer. Use DAX to display text dynamically based on the selected language.

---

### 125. What are report themes, and how can they be customized?  
**Answer:**  
Report themes define visual styles—colors, fonts, etc. They can be customized via a JSON file and imported to ensure consistent design.

---

### 126. How do you create drill-down reports without using hierarchy fields directly?  
**Answer:**  
Simulate drill-downs using:  
- Bookmarks and buttons  
- Page navigation  
- Field parameters or dynamic visuals with DAX

---

### 127. What is a field parameter and how does it help in visualizing dynamic dimensions or measures?  
**Answer:**  
Field Parameters allow users to switch dimensions or measures in visuals dynamically. Enhances interactivity and flexibility in report exploration.

---

### 128. How can you implement report navigation inside Power BI reports?  
**Answer:**  
Navigation can be built using:  
- Buttons with **Page navigation** actions  
- Bookmarks  
- Drill-through pages with back buttons

---

### 129. How can you enable users to export report visuals or pages from Power BI?  
**Answer:**  
Users can export:  
- Visuals to image (PNG) via right-click  
- Pages to PDF or PowerPoint from the service  
- Underlying data using “Export data” (if permitted)

---

### 130. What are slicer sync options, and how do they affect reporting?  
**Answer:**  
Slicer sync allows a slicer to control filters across pages. Options include:  
- Showing slicer only on selected pages  
- Syncing values even when hidden  
Helps maintain cross-page consistency.

---

### 131. How do you design reports for mobile view in Power BI?  
**Answer:**  
Use the Mobile Layout View to rearrange and resize visuals for mobile devices. Best practices:  
- Prioritize key visuals  
- Use KPIs/cards  
- Minimize scrolling  
- Ensure text readability

---

### 132. What are the differences between live connection and import mode when it comes to report responsiveness?  
**Answer:**  
- **Import Mode** – Data is cached, enabling fast visuals and interactions.  
- **Live Connection** – Data fetched in real-time; slower but ensures current data.

---

### 133. What are the benefits of using tooltip fields versus tooltip pages?  
**Answer:**  
- **Tooltip fields** – Simple, quick setup for contextual data.  
- **Tooltip pages** – Offer rich, customizable insights with more flexibility and visual depth.

---

### 134. How can you allow users to toggle between different chart types in Power BI?  
**Answer:**  
Chart toggling can be implemented using:  
- Field Parameters  
- Bookmarks  
- DAX visibility logic with selection tables

---

### 135. How do you use the "Show As Table" feature in visuals, and when is it helpful?  
**Answer:**  
"Show As Table" (right-click on a visual) displays the tabular data behind a visual. Useful for:  
- Ad hoc analysis  
- Validating summaries  
- Enhancing data transparency

---

### 136. What considerations should you keep in mind when designing accessible Power BI reports?  
**Answer:**  
To ensure accessibility:  
- Use strong contrast for text/background  
- Add alt text to visuals  
- Enable keyboard navigation  
- Avoid color dependency; use labels/icons  
Use the **Accessibility Checker** in Power BI Desktop for compliance.

---
