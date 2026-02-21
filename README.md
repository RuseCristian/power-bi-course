# 📊 Power BI Data Analytics - Learning Journey

My hands-on Power BI learning repository featuring interactive dashboards, data transformations, and analytics using real-world job market data from 2024.

[![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)](https://docs.microsoft.com/en-us/dax/)
[![M Language](https://img.shields.io/badge/M%20Language-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)](https://docs.microsoft.com/en-us/powerquery-m/)

## 🎯 What I Built

- **📊 Interactive Dashboards**: Multi-page analytical dashboards with drill-through pages
- **🔄 Data Pipelines**: Automated ETL processes using Power Query
- **📈 Advanced Analytics**: DAX measures and complex calculations
- **🎨 Visual Storytelling**: Professional visualizations with cohesive design

![Power BI Dashboard Overview](images/pbi%202.8.png)
_Comprehensive Data Jobs Dashboard_

## 📖 Learning Path

### 1️⃣ Grand Tour - Power BI Fundamentals

Introduction to Power BI Desktop, dashboard creation, and data import basics.

![Power BI Interface](images/pbi%201.2.png)
_Building my first dashboard_

---

### 2️⃣ Visualizations - Chart Types & Design

**Key Visualizations Built**:

- **Stacked Bar Chart**: Highest-paying job titles using **median salary** (median avoids outlier skew, providing more realistic compensation insights than averages)
- **Clustered Column Chart**: Monthly salary trends across top countries
- **Line Charts**: Trend analysis with min/max indicators and forecasting
- **Maps**: Geographic distribution with ArcGIS integration
- **Tables & Matrices**: Conditional formatting and drill-through capabilities
- **Cards & KPIs**: Key metrics with gauge and trend indicators

![Visualizations - Bar Charts](images/pbi%202.1.png)
_Salary analysis by job title_

![Visualizations - Multiple Charts](images/pbi%202.2.png)
_Degree requirements analysis_

![Visualizations - Advanced](images/pbi%202.3.png)
_Line charts with analytics_

**Interactive Features**:

- Advanced filtering (Y-axis filters for "data" job titles only)
- Slicers: Multi-select, dropdown, search, synced across pages
- Edit interactions for controlled cross-filtering
- Drill-through pages for detailed analysis

![Slicers & Filters](images/pbi%202.6.png)
_Interactive slicers configuration_

![Map Visualizations](images/pbi%202.7.png)
_Geographic distribution of jobs_

**Design Principles**: Cohesive color schemes, consistent tooltips, professional layering

![Dashboard Design](images/pbi%202.9.png)
_Final comprehensive dashboard_

---

### 3️⃣ Power Query - Data Transformation & ETL

**Data Sources Explored**:

- Web scraping (Wikipedia GDP tables)
- Folder imports with auto-refresh
- Google BigQuery database connections
- Monthly Excel files (combined 12 months into one dataset)

**Transformations**:

- Data cleaning and normalization
- Conditional columns and text standardization
- Append queries (union monthly reports)
- Merge queries (star schema → flat table)

**M Language**: Custom transformations executed at **data import time** (vs. DAX at query runtime)

![Power Query Measures](images/pbi%203.1%20measures.png)
_Power Query transformations_

![Advanced Measures](images/pbi%203.2%20measures.png)
_DAX measures setup_

---

### 4️⃣ DAX - Data Analysis Expressions

**Core Concepts**:

- **Calculated Columns** (computed at data import, stored in model) vs **Measures** (calculated at query runtime, more efficient)
- Row Context, Filter Context, Query Context
- **Best Practice**: Use `_Measures` table for centralized measure management

**Measures Created**:

- Total Jobs Count, Median Salary, Degree Requirements %
- Month-over-Month Growth, Top N filtering

**Parameters**: What-if scenarios, dynamic thresholds

![DAX Parameters](images/pbi%203.3%20measures%20parameter.png)
_Parameter configuration for dynamic analysis_

---

## 🛠️ Tech Stack

- **Power BI Desktop** - Dashboard development
- **Power Query (M Language)** - ETL and data transformation (executes at data import time)
- **DAX** - Measures and calculations (executes at query runtime)
- **Data Sources**: CSV, Excel, Web scraping, Google BigQuery
