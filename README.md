# Power BI Data Analytics - Learning Journey

My hands-on Power BI learning repository featuring interactive dashboards, data transformations, and analytics using real-world job market data from 2024.

**Course Followed**: [Power BI for Data Analytics - Full Course by Luke Barousse](https://www.youtube.com/watch?v=h_XYGj5pWeI)

[![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)](https://docs.microsoft.com/en-us/dax/)
[![M Language](https://img.shields.io/badge/M%20Language-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)](https://docs.microsoft.com/en-us/powerquery-m/)

## What I Built

- **Interactive Dashboards**: Multi-page analytical dashboards with drill-through pages
- **Data Pipelines**: Automated ETL processes using Power Query
- **Advanced Analytics**: DAX measures and complex calculations
- **Visual Storytelling**: Professional visualizations with cohesive design

![Power BI Dashboard Overview](images/pbi%202.8.png)
_Comprehensive Data Jobs Dashboard_

---

## Learning Path

### Chapter 1: Grand Tour - Power BI Fundamentals

Introduction to Power BI Desktop interface and core capabilities. Explored navigation between Report, Data, and Model views. Learned data import from CSV files and built my first dashboard understanding the end-to-end workflow.

![Power BI Interface](images/pbi%201.1.png)
_Power BI Desktop interface overview_

![Building First Dashboard](images/pbi%201.2.png)
_Creating my first dashboard with job data_

---

### Chapter 2: Visualizations - Chart Types & Design

Mastered Power BI's visualization library, understanding when to use each chart type and how to configure them properly.

**Key Visualizations**:

- **Stacked Bar Chart**: Highest-paying job titles using **median salary** (avoids outlier skew vs. averages)
- **Clustered Column Chart**: Monthly salary trends across top countries
- **Line Charts**: Trend analysis with min/max indicators, Analytics pane features

![Visualizations - Bar Charts](images/pbi%202.1.png)
_Salary analysis by job title using median values_

![Visualizations - Advanced](images/pbi%202.3.png)
_Line charts with analytics pane features_

![Visualizations - Multiple Charts](images/pbi%202.2.png)
_Degree requirements breakdown_

![Charts Comparison](images/pbi%202.4.png)
_Comparing different chart types_

![Stacked Charts](images/pbi%202.5.png)
_Stacked column and percentage charts_

**Interactive Features**:

- Advanced filtering (Y-axis filters for "data" job titles only)
- Multiple slicer types (multi-select, dropdown, search) synced across pages
- Edit interactions to control visual cross-filtering

![Slicers & Filters](images/pbi%202.6.png)
_Interactive slicers configuration_

- **Maps**: Standard map visualizations and ArcGIS Maps integration with custom tooltips
- **Tables & Matrices**: Conditional formatting and drill-through functionality
- **Cards & KPIs**: Simple cards, multi-row cards, gauge cards, KPI cards with trend indicators

![Map Visualizations](images/pbi%202.9.png)
_Geographic distribution of job opportunities_

**Design & Drill-Through**:

Maintained cohesive color schemes, consistent tooltips, and professional layering. Implemented drill-through functionality allowing users to navigate from summary dashboard to detailed analysis pages.

![Main Dashboard](images/pbi%202.7.png)
_Main dashboard with drill-through capabilities_

---

### Chapter 3: Power Query - Data Transformation & ETL

Power Query is Power BI's ETL engine. Learned that clean, well-structured data is the foundation of good dashboards. Power Query Editor provides visual interface powered by M Language behind the scenes.

**Data Sources**: Web scraping (Wikipedia tables), folder imports with auto-refresh, Google BigQuery, monthly Excel files

**Transformations**: Data cleaning, conditional columns, text standardization, append queries (union monthly reports), merge queries (SQL-like joins), star schema ↔ flat table conversion

**M Language**: Executes at **data import time** (vs. DAX at query runtime). Perfect for data transformation and shaping.

![Power Query Measures](images/pbi%203.1%20measures.png)
_Power Query transformations_

![Advanced Measures](images/pbi%203.2%20measures.png)
_Setting up measures and relationships_

---

### Chapter 4: DAX - Data Analysis Expressions

DAX is Power BI's formula language for custom calculations. Learned to write measures and calculated columns to derive insights not directly available in raw data.

**Core Concepts**:

- **Calculated Columns** (data import, stored, consumes memory) vs **Measures** (query runtime, dynamic, efficient)
- **Context Types**: Row Context, Filter Context, Query Context
- **Best Practice**: `_Measures` table for centralized measure management

**Measures Created**: Total job counts, median/average salaries, degree requirement percentages, month-over-month growth, Top N filtering

**Parameters**: What-if parameters for real-time scenario analysis, dynamic thresholds for conditional formatting

![DAX Parameters](images/pbi%203.3%20measures%20parameter.png)
_Parameter configuration for dynamic analysis_

---

## Tech Stack

- **Power BI Desktop** - Dashboard development
- **Power Query (M Language)** - ETL and data transformation (executes at data import time)
- **DAX** - Measures and calculations (executes at query runtime)
- **Data Sources**: CSV, Excel, Web scraping, Google BigQuery
