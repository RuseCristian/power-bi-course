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

![Power BI Dashboard Overview](images/pbi%201.1.png)
*Dashboard Interface - Getting Started*

## 📖 Learning Path

### 1️⃣ Grand Tour - Power BI Fundamentals
Introduction to Power BI Desktop, dashboard creation, and data import basics.

![Power BI Interface](images/pbi%201.2.png)
*Building my first dashboard*

---

### 2️⃣ Visualizations - Chart Types & Design

**Key Visualizations Built**:
- **Stacked Bar Chart**: Highest-paying job titles using **median salary** (avoiding outlier skew from averages)
- **Clustered Column Chart**: Monthly salary trends across top countries
- **Line Charts**: Trend analysis with min/max indicators and forecasting
- **Maps**: Geographic distribution with ArcGIS integration
- **Tables & Matrices**: Conditional formatting and drill-through capabilities
- **Cards & KPIs**: Key metrics with gauge and trend indicators

![Visualizations - Bar Charts](images/pbi%202.1.png)
*Salary analysis by job title*

![Visualizations - Multiple Charts](images/pbi%202.2.png)
*Degree requirements analysis*

![Visualizations - Advanced](images/pbi%202.3.png)
*Line charts with analytics*

**Interactive Features**:
- Advanced filtering (Y-axis filters for "data" job titles only)
- Slicers: Multi-select, dropdown, search, synced across pages
- Edit interactions for controlled cross-filtering
- Drill-through pages for detailed analysis

![Slicers & Filters](images/pbi%202.6.png)
*Interactive slicers configuration*

![Map Visualizations](images/pbi%202.7.png)
*Geographic distribution of jobs*

**Design Principles**: Cohesive color schemes, consistent tooltips, professional layering

![Dashboard Design](images/pbi%202.9.png)
*Final comprehensive dashboard*

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

**M Language**: Custom transformations at data import time

![Power Query Measures](images/pbi%203.1%20measures.png)
*Power Query transformations*

![Advanced Measures](images/pbi%203.2%20measures.png)
*DAX measures setup*

---

### 4️⃣ DAX - Data Analysis Expressions

**Core Concepts**:
- **Calculated Columns** (data import) vs **Measures** (query runtime)
- Row Context, Filter Context, Query Context
- **Best Practice**: `_Measures` table for centralized measure management

**Measures Created**:
- Total Jobs Count, Median Salary, Degree Requirements %
- Month-over-Month Growth, Top N filtering

**Parameters**: What-if scenarios, dynamic thresholds

![DAX Parameters](images/pbi%203.3%20measures%20parameter.png)
*Parameter configuration for dynamic analysis*

---

## 🚀 Featured Projects

### Project 1: Multi-Page Data Jobs Dashboard
Multi-page dashboard with drill-through functionality, interactive slicers, and 15+ synchronized visualizations.

**Highlights**: Market overview, salary analysis (median-based), geographic distribution, degree requirements

### Project 2: Optimized Dashboard 2.0
Single-page dashboard with star schema data model and advanced DAX measures for improved performance.

---

## 🛠️ Tech Stack

- **Power BI Desktop** - Dashboard development
- **Power Query (M Language)** - ETL and data transformation
- **DAX** - Measures and calculations
- **Data Sources**: CSV, Excel, Web scraping, Google BigQuery

---

## 🚀 Quick Start

1. **Install Power BI Desktop**: [Download here](https://powerbi.microsoft.com/desktop/)
2. **Clone the repo**:
   ```bash
   git clone https://github.com/RuseCristian/power-bi-course.git
   ```
3. **Open any `.pbix` file** and click "Enable Content"

> ⚠️ **Note**: Some large files (>100MB) use Git LFS. Install [Git LFS](https://git-lfs.github.com/) and run `git lfs pull` if needed.

---

## 📁 Repository Structure

```
power-bi-course/
├── README.md
├── chapter 1.pbix - 4.3.pbix          # Course progression files
├── Data/monthly jobs/                  # Practice datasets (Jan-Jul)
├── images/                             # Screenshots & documentation
└── PowerBI_Data_Analytics_Course/      # Complete course materials
    ├── _Project_1/                     # Multi-page dashboard
    ├── _Project_2/                     # Optimized dashboard
    ├── 1_Grand_Tour/                   # Module 1: Basics
    ├── 2_Visualizations/               # Module 2: Charts
    ├── 3_Power_Query/                  # Module 3: ETL
    ├── 4_DAX/                          # Module 4: Analytics
    ├── Data/                           # Course datasets
    │   ├── monthly_files/              # 12 monthly Excel files
    │   └── star_schema_files/          # Normalized data
    ├── Problems/                       # Practice exercises
    └── Resources/                      # Supporting materials
```

---

## � Key Takeaways

### Why Median Over Average?
I consistently used **median instead of average** for salary analysis because:
- **Resistant to outliers** (avoids skew from extreme salaries)
- **More realistic** representation of typical compensation
- **Better reflects** actual market conditions

### M Language vs DAX
- **M Language**: Executes at data import time (ETL layer)
- **DAX**: Executes at query runtime (Analytics layer)

### Best Practices Learned
- Use `_Measures` table for centralized measure management
- Prefer measures over calculated columns for better performance
- Maintain cohesive color schemes across dashboards
- Sync slicers for consistent user experience

---

## 👤 Author

**Cristian Ruse**
- GitHub: [@RuseCristian](https://github.com/RuseCristian)
- Repository: [power-bi-course](https://github.com/RuseCristian/power-bi-course)

---

⭐ **If you found this helpful, please star the repo!** ⭐
