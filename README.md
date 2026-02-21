# Power BI Data Analytics - Learning Journey

My hands-on Power BI learning repository featuring interactive dashboards, data transformations, and analytics using real-world job market data from 2024.

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

This chapter introduces the Power BI Desktop interface and its core capabilities. I explored the main components of the application, understanding how to navigate between different views (Report, Data, and Model). The focus was on getting comfortable with the workspace, understanding how to import data from CSV files, and creating basic visualizations. I built my first simple dashboard to understand the end-to-end workflow from data import to visualization.

![Power BI Interface](images/pbi%201.1.png)
_Power BI Desktop interface overview_

![Building First Dashboard](images/pbi%201.2.png)
_Creating my first dashboard with job data_

---

### Chapter 2: Visualizations - Chart Types & Design

This chapter was dedicated to mastering Power BI's extensive visualization library. I systematically explored each chart type, understanding when to use each one and how to configure them properly. The emphasis was on creating meaningful visualizations that tell a story with the data, not just displaying numbers. I learned the importance of choosing the right chart type for the data and the insights I wanted to communicate.

**Key Visualizations Built**:

- **Stacked Bar Chart**: Analyzed highest-paying job titles using **median salary** instead of average. The median provides more realistic compensation insights because it's resistant to outliers - a few extremely high or low salaries won't skew the results like they would with averages.

![Visualizations - Bar Charts](images/pbi%202.1.png)
_Salary analysis by job title using median values_

- **Clustered Column Chart**: Displayed monthly salary trends across the top countries with the most job postings, allowing for easy comparison between geographic markets.

![Visualizations - Multiple Charts](images/pbi%202.2.png)
_Degree requirements breakdown - positions requiring degrees vs. those that don't_

- **Line Charts**: Created trend analysis with min/max indicators and forecasting capabilities. Explored the Analytics pane to add reference lines, trend lines, and statistical insights directly on visualizations.

![Visualizations - Advanced](images/pbi%202.3.png)
_Line charts with analytics pane features_

![Charts Comparison](images/pbi%202.4.png)
_Comparing different chart types for the same data_

![Stacked Charts](images/pbi%202.5.png)
_Stacked column and percentage charts for composition analysis_

**Interactive Features**:

Learned how to make dashboards truly interactive by implementing advanced filtering techniques. Used Y-axis filters to exclude non-data roles (like general software engineering or machine learning positions) by specifying that job titles must contain the word "data". Implemented multiple slicer types including multi-select, dropdown, and search capabilities, then synchronized them across all pages for a consistent user experience.

![Slicers & Filters](images/pbi%202.6.png)
_Interactive slicers with multi-select and search functionality_

- **Maps**: Explored both standard map visualizations and ArcGIS Maps integration for geographic analysis. Learned how to customize tooltips to provide additional context when hovering over locations.

![Map Visualizations](images/pbi%202.7.png)
_Geographic distribution of job opportunities_

- **Tables & Matrices**: Implemented conditional formatting to highlight important values and trends. Set up drill-through functionality on table rows to navigate to detailed analysis pages.

- **Cards & KPIs**: Created simple cards for key metrics, multi-row cards for grouped data, gauge cards for progress indicators, and KPI cards with trend indicators showing performance over time.

![Card Visuals](images/pbi%202.8.png)
_Various card types displaying key metrics_

**Design Principles**:

Focused on maintaining a cohesive color scheme throughout the entire dashboard to avoid visual distraction. Learned that consistent tooltip formatting and professional layering of visuals creates a more polished and user-friendly experience. Implemented edit interactions to control how visuals cross-filter each other, preventing unwanted filtering behavior.

![Dashboard Design](images/pbi%202.9.png)
_Final comprehensive dashboard with cohesive design_

---

### Chapter 3: Power Query - Data Transformation & ETL

This chapter focused on Power Query, Power BI's ETL (Extract, Transform, Load) engine. I learned that clean, well-structured data is the foundation of any good dashboard. Power Query Editor provides a visual interface for data transformation, but it's powered by M Language behind the scenes. The key concept here is that all these transformations happen at data import time, before the data enters the data model.

**Data Sources Explored**:

- **Web scraping**: Tested importing data directly from web URLs, successfully extracting GDP data from Wikipedia tables
- **Folder imports**: Set up automated imports that dynamically update when new files are added to a folder
- **Google BigQuery**: Connected to cloud databases for enterprise-scale data access
- **Monthly Excel files**: Combined 12 separate monthly reports into a single consolidated dataset using append queries

**Transformations**:

Performed extensive data cleaning including removing duplicates, handling null values, and standardizing data types. Created conditional columns to categorize data, used text functions for capitalization and replacing values. Learned the difference between referencing queries (creates a dependency) versus duplicating queries (creates an independent copy).

- **Append queries**: Combined multiple tables with identical schemas into one unified table (used for monthly reports)
- **Merge queries**: Performed joins between tables, similar to SQL joins, to combine related data from different sources
- **Data modeling**: Converted between star schema (normalized with fact and dimension tables) and flat table structures depending on analysis needs

**M Language**:

M Language is the formula language behind Power Query. The critical distinction is that M Language executes at **data import time** (when you refresh the data), while DAX executes at **query runtime** (when you interact with visuals). This makes M Language perfect for data transformation and shaping, while DAX is better for calculations and aggregations.

![Power Query Measures](images/pbi%203.1%20measures.png)
_Power Query transformations in action_

![Advanced Measures](images/pbi%203.2%20measures.png)
_Setting up measures and data relationships_

---

### Chapter 4: DAX - Data Analysis Expressions

DAX (Data Analysis Expressions) is Power BI's formula language for creating custom calculations. This chapter taught me how to write measures and calculated columns to derive insights that aren't directly available in the raw data. Understanding the difference between calculated columns and measures is crucial for building efficient data models.

**Core Concepts**:

- **Calculated Columns vs. Measures**:
  - Calculated columns are computed once at data import time, stored in the data model, and consume memory. Use them when you need row-by-row calculations that don't change based on user interactions.
  - Measures are calculated dynamically at query runtime based on the current filter context. They're more efficient because they're not stored, and they respond to slicers, filters, and user interactions. Prefer measures whenever possible.

- **Context Types**:
  - **Row Context**: Iterates through each row individually (used in calculated columns)
  - **Filter Context**: Applied by slicers, filters, and visual selections - determines what data is visible
  - **Query Context**: The overall environment in which calculations are executed

- **Best Practice - The \_Measures Table**: Created a dedicated table called `_Measures` (with underscore prefix to appear at the top of field list) that contains no data, only measures. This organizational approach makes it much easier to find and maintain all calculations in one place, rather than having them scattered across different data tables.

**Measures Created**:

Developed a library of reusable measures including total job counts, median and average salaries, percentage of jobs requiring degrees, month-over-month growth calculations, and Top N filtering logic for dynamic ranking visualizations.

**Parameters**:

Learned to create what-if parameters that allow users to adjust values and see results change in real-time. Implemented dynamic thresholds for conditional formatting that adapt based on user input. This makes dashboards more interactive and allows for scenario analysis.

![DAX Parameters](images/pbi%203.3%20measures%20parameter.png)
_Parameter configuration for dynamic scenario analysis_

---

## Tech Stack

- **Power BI Desktop** - Primary dashboard development environment
- **Power Query (M Language)** - ETL and data transformation layer (executes at data import time)
- **DAX (Data Analysis Expressions)** - Measures and calculations (executes at query runtime)
- **Data Sources**: CSV files, Excel workbooks, Web scraping, Google BigQuery
