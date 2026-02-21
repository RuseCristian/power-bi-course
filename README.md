# 📊 Power BI Data Analytics - Learning Journey

A comprehensive repository documenting my journey learning Power BI for data analytics, featuring hands-on projects, visualizations, and data transformation techniques using real-world job market data.

[![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DAX](https://img.shields.io/badge/DAX-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)](https://docs.microsoft.com/en-us/dax/)
[![M Language](https://img.shields.io/badge/M%20Language-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)](https://docs.microsoft.com/en-us/powerquery-m/)

## 📚 Table of Contents
- [Overview](#-overview)
- [Course Structure](#-course-structure)
- [Key Learning Outcomes](#-key-learning-outcomes)
- [Projects & Dashboards](#-projects--dashboards)
- [Tools & Technologies](#-tools--technologies)
- [Getting Started](#-getting-started)
- [Repository Structure](#-repository-structure)

## 🎯 Overview

This repository contains all materials from my Power BI learning journey, including practice files, dashboards, and data transformation projects. The course focuses on practical, real-world applications using a dataset of data science job postings from 2024.

### What I Built
- **Interactive Dashboards**: Multi-page analytical dashboards with drill-through functionality
- **Data Pipelines**: Automated ETL processes using Power Query
- **Advanced Analytics**: DAX measures for complex calculations and insights
- **Visual Storytelling**: Professional visualizations following best practices

## 📖 Course Structure

### 1️⃣ Grand Tour - Power BI Fundamentals
**Focus**: Introduction to Power BI interface, tools, and capabilities

**What I Learned**:
- Power BI Desktop interface and navigation
- Basic dashboard creation workflow
- Data import from CSV files
- Simple visualizations and formatting
- Publishing and sharing dashboards

**Files**: 
- `chapter 1.pbix`
- `PowerBI_Data_Analytics_Course/1_Grand_Tour/`

---

### 2️⃣ Visualizations - Mastering Visual Elements
**Focus**: Deep dive into Power BI's visualization capabilities

#### 📊 Chart Types Explored

**Bar & Column Charts**:
- **Stacked Bar Chart**: Analyzed highest-paying job titles with median yearly salary
  - *Key Insight*: Used **median instead of average** salary to avoid skewed results from outliers, providing a more realistic picture of compensation
- **Clustered Column Chart**: Displayed average yearly salary per month across top 4 countries
- **Stacked Column Chart**: Compared degree vs. no-degree requirements by job position
- **Stacked Percentage Chart**: Visualized degree requirement distributions as percentages

**Advanced Filters**:
- Implemented Y-axis filtering to exclude non-data roles (e.g., software engineering, machine learning)
- Used "contains" operator to filter job titles containing "data"

**Line Charts & Analytics**:
- Trend analysis over time
- Min/Max indicators
- Analytics pane features (trendlines, forecasting)
- Drill-down functionality across time hierarchies

**Distribution Charts**:
- **Pie & Donut Charts**: Simple proportion displays
- **Treemap**: Hierarchical data visualization
- **Scatter Charts**: Correlation analysis

**Geospatial Visualizations**:
- Standard Map charts
- ArcGIS Maps integration
- Custom tooltips for enhanced context

**Data Tables & Matrices**:
- Conditional formatting techniques
- Drill-through on table rows
- Matrix hierarchies and subtotals

**KPI & Card Visuals**:
- Simple cards for key metrics
- Multi-row cards for grouped data
- Gauge cards for progress indicators
- KPI cards with trend indicators

**Interactive Elements**:
- **Slicers**: Multi-select, single-select, dropdown, search, and hierarchy slicers
- **Sync Slicers**: Cross-page filtering
- Clear all filters button
- Edit Interactions: Controlled visual cross-filtering behavior

#### 🎨 Design Principles
- Maintained cohesive color scheme across entire dashboard
- Implemented consistent tooltip formatting
- Layered visuals for professional appearance
- Created drill-through page for detailed analysis

**Files**:
- `chapter 2.pbix`
- `PowerBI_Data_Analytics_Course/2_Visualizations/`

---

### 3️⃣ Power Query - Data Transformation & ETL
**Focus**: Data import, transformation, and preparation using Power Query Editor

#### 📥 Data Loading Methods

**Web Data Sources**:
- Tested direct web scraping from Wikipedia (GDP by country)
- URL: `https://en.wikipedia.org/wiki/List_of_countries_by_GDP_(nominal)`
- HTML table parsing and cleaning

**Folder Import**:
- Automated data loading from folders
- Dynamic updates when new files are added
- Batch processing of monthly Excel files
- Combined 12 monthly reports into single dataset

**Database Connections**:
- Google BigQuery integration
- Example: America Health Ratings dataset
- Direct database queries

#### 🔧 Data Transformations

**Basic Transformations**:
- Column renaming and reordering
- Data type conversions
- Remove duplicates and nulls
- Split and merge columns

**Advanced Transformations** (`chapter 3.3`):
- Created normalized **Job Type** table (Full-time, Part-time, Contract, etc.)
- Cleaned job skills data using:
  - Multiple conditional columns
  - Text capitalization standardization
  - Replace values operations
- Reference queries vs. duplicate queries
- Cross-referencing between tables

#### 🔗 Query Operations

**Append Queries**:
- Combined monthly job posting reports (Jan-Dec 2024)
- Union operations for identical schemas
- Append vs. Append Queries as New

**Merge Queries**:
- Converted star schema to flat table structure
- Join types: Inner, Left Outer, Right Outer, Full Outer
- Expanded nested tables

#### ⚙️ M Language
**Concept**: M Language executes at **data import time** (vs. DAX at query runtime)

**Applications**:
- Custom column transformations
- Advanced date/time calculations
- Column from Example feature
- Custom functions
- Query parameters

**Files**:
- `chapter 3.1 different data loadings.pbix`
- `chapter 3.2 pwqr query append.pbix`
- `chapter 3.3 pwqr merging, measures, parameters.pbix`
- `PowerBI_Data_Analytics_Course/3_Power_Query/`

---

### 4️⃣ DAX - Data Analysis Expressions
**Focus**: Creating calculations and measures for advanced analytics

#### 📐 Core Concepts

**Calculated Columns vs. Measures**:
- **Calculated Columns**: Computed at data import, stored in data model, consumes memory
- **Measures**: Calculated at query runtime, dynamic based on filter context, more efficient

**Context Types**:
- **Row Context**: Iterates row-by-row (used in calculated columns)
- **Filter Context**: Applied by slicers, filters, and visual selections
- **Query Context**: Entire query execution environment

#### 📏 Explicit Measures
**Best Practice**: Created dedicated `_Measures` table for all explicit measures

**Organizational Benefits**:
- Centralized measure management
- Easier to find and maintain
- Cleaner field list in report view
- No data storage (virtual table)

**Sample Measures Created**:
- Total Jobs Count
- Average Salary (Mean vs. Median)
- Jobs with Degree Requirements (%)
- Month-over-Month Growth
- Top N filtering

#### 🎛️ Parameters
- What-if parameters for scenario analysis
- Dynamic thresholds for conditional formatting
- User-controlled calculations

**Files**:
- `chapter 4.1.pbix`
- `chapter 4.2 explicit meas.pbix`
- `chapter 4.3 param.pbix`
- `PowerBI_Data_Analytics_Course/4_DAX/`

---

## 🎯 Key Learning Outcomes

### Data Analysis
- ✅ Statistical analysis using median vs. average for accurate insights
- ✅ Filtering and segmentation techniques
- ✅ Time-series analysis and trend identification
- ✅ Geospatial data visualization

### Data Engineering
- ✅ ETL pipeline creation with Power Query
- ✅ Data normalization and denormalization
- ✅ Automated data refresh workflows
- ✅ Star schema and flat file design patterns

### Business Intelligence
- ✅ Dashboard design principles and best practices
- ✅ Interactive storytelling with drill-through pages
- ✅ KPI tracking and performance monitoring
- ✅ User experience optimization with slicers and filters

### Technical Skills
- ✅ **M Language**: Data transformation at import time
- ✅ **DAX**: Dynamic calculations and measures
- ✅ **Power Query**: ETL and data modeling
- ✅ **Visual Design**: Color theory, layering, and professional aesthetics

---

## 🚀 Projects & Dashboards

### Project 1: Comprehensive Data Jobs Dashboard
**Type**: Multi-page dashboard with drill-through functionality

**Features**:
- Market overview page with key metrics
- Salary analysis by job title (median-based)
- Geographic distribution of opportunities
- Degree requirement breakdowns
- Interactive slicers synced across all pages
- Drill-through detail page for deep-dive analysis

**Technical Highlights**:
- 15+ visualizations with custom interactions
- DAX measures for dynamic calculations
- Advanced filtering logic
- Professional color scheme and tooltips

**File**: `PowerBI_Data_Analytics_Course/_Project_1/Data_Jobs_Dashboard.pbix`

---

### Project 2: Data Jobs Dashboard 2.0
**Type**: Single-page focused dashboard with star schema

**Features**:
- Streamlined insights on one page
- Star schema data model (fact + dimension tables)
- Advanced DAX expressions
- Optimized performance for large datasets

**Technical Highlights**:
- Normalized data structure
- Complex measure calculations
- Efficient data model design
- Enhanced visual hierarchy

**File**: `PowerBI_Data_Analytics_Course/_Project_2/Data_Jobs_Dashboard_2.0.pbix`

---

## 🛠️ Tools & Technologies

### Software
- **Power BI Desktop**: Primary development environment
- **Power Query Editor**: Data transformation and ETL
- **DAX Studio**: (Optional) Advanced DAX optimization

### Languages & Frameworks
- **M Language**: Power Query transformations
- **DAX (Data Analysis Expressions)**: Measures and calculated columns

### Data Sources
- **CSV Files**: Flat file format (job_postings_flat.csv - *Note: 136 MB, not on GitHub*)
- **Excel Files**: Monthly reports and aggregated data
- **Web Scraping**: Wikipedia and other web sources
- **Google BigQuery**: Cloud database connections

### Data Schema
- **Flat Schema**: Single denormalized table
- **Star Schema**: Fact table + dimension tables (company, skills, job_skills_bridge)

---

## 🚀 Getting Started

### Prerequisites
- **Power BI Desktop** (Free) - [Download here](https://powerbi.microsoft.com/desktop/)
- **Windows 10/11** or **Windows Server 2016+**
- **4 GB RAM minimum** (8 GB+ recommended for large datasets)

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/RuseCristian/power-bi-course.git
   cd power-bi-course
   ```

2. **Download Large Files** (Optional):
   > ⚠️ **Note**: Some files exceed GitHub's 100 MB limit and are tracked with Git LFS
   
   If you need the full `job_postings_flat.csv` (136 MB):
   - Install [Git LFS](https://git-lfs.github.com/)
   - Run: `git lfs pull`

3. **Open Power BI Files**:
   - Navigate to desired chapter folder
   - Double-click any `.pbix` file
   - Click "Enable Content" when prompted

### Quick Start Guide

#### Option 1: Follow the Course
Start with `chapter 1.pbix` and progress through chapters 1-4

#### Option 2: Explore Projects
Jump directly to the completed dashboards:
- `PowerBI_Data_Analytics_Course/_Project_1/Data_Jobs_Dashboard.pbix`
- `PowerBI_Data_Analytics_Course/_Project_2/Data_Jobs_Dashboard_2.0.pbix`

#### Option 3: Practice Problems
Check out `PowerBI_Data_Analytics_Course/Problems/` for hands-on exercises

---

## 📁 Repository Structure

```
power-bi-course/
│
├── README.md                          # This file
│
├── chapter 1.pbix                     # Grand Tour - Basic dashboard
├── chapter 2.pbix                     # Visualizations practice
├── chapter 3.1 different data loadings.pbix  # Power Query basics
├── chapter 3.2 pwqr query append.pbix        # Append operations
├── chapter 3.3 pwqr merging, measures, parameters.pbix  # Advanced transforms
├── chapter 4.1.pbix                   # DAX introduction
├── chapter 4.2 explicit meas.pbix     # Explicit measures
├── chapter 4.3 param.pbix             # Parameters
│
├── Data/                              # Personal practice data
│   └── monthly jobs/                  # Monthly Excel files (Jan-Jul)
│       ├── job_postings_01-2024.xlsx
│       ├── job_postings_02-2024.xlsx
│       └── ...
│
├── images/                            # Screenshot documentation
│   ├── pbi 1.1.png
│   ├── pbi 2.1.png
│   └── ...
│
└── PowerBI_Data_Analytics_Course/     # Complete course materials
    ├── README.md                      # Detailed course documentation
    │
    ├── _Project_1/                    # Multi-page dashboard
    │   ├── Data_Jobs_Dashboard.pbix
    │   └── README.md
    │
    ├── _Project_2/                    # Single-page optimized dashboard
    │   ├── Data_Jobs_Dashboard_2.0.pbix
    │   └── README.md
    │
    ├── 1_Grand_Tour/                  # Module 1: Introduction
    │   ├── 1.1_PBI_App_Intro.pbix
    │   └── 1.2_Dashboard_Build.pbix
    │
    ├── 2_Visualizations/              # Module 2: Charts & Visuals
    │   └── 2_Visualizations.pbix
    │
    ├── 3_Power_Query/                 # Module 3: ETL & Transformations
    │   ├── 3.1_Power_Query_Intro.pbix
    │   ├── 3.1_Power_Query__Intro(BigQuery Demo).pbix
    │   ├── 3.2_Power_Query_Editor.pbix
    │   ├── 3.3_Project2_Import.pbix
    │   ├── 3.4_Adv_Transformations.pbix
    │   ├── 3.5_Append.pbix
    │   ├── 3.5_Merge.pbix
    │   └── 3.6_M_Language.pbix
    │
    ├── 4_DAX/                         # Module 4: DAX & Measures
    │   ├── 4.1_DAX_Intro.pbix
    │   ├── 4.2_Explicit_Measures.pbix
    │   └── 4.3_Parameters.pbix
    │
    ├── Data/                          # Course datasets
    │   ├── job_postings_flat.csv      # ⚠️ 136 MB - Use Git LFS
    │   ├── job_postings_monthly.xlsx
    │   ├── README.md
    │   ├── monthly_files/             # Individual monthly files
    │   │   ├── job_postings_01-2024.xlsx
    │   │   ├── job_postings_02-2024.xlsx
    │   │   └── ... (Jan-Dec 2024)
    │   │
    │   └── star_schema_files/         # Normalized database
    │       ├── company_dim.csv
    │       ├── job_postings_fact.csv  # ⚠️ 75 MB
    │       ├── skills_dim.csv
    │       └── skills_job_dim.csv
    │
    ├── Problems/                      # Practice exercises with solutions
    │   ├── 1_Grand_Tour/
    │   ├── 2_Visualizations/
    │   ├── 3_Power_Query/
    │   └── 4_DAX/
    │
    └── Resources/                     # Supporting materials
        ├── images/
        └── Project_Examples/
```

---

## 📊 Dataset Information

### Data Source
Real-world data science job postings from 2024, including:
- Job titles and descriptions
- Salary information (yearly compensation)
- Location data (country, city)
- Required skills and technologies
- Education requirements (degree vs. no degree)
- Employment type (Full-time, Part-time, Contract)
- Company information
- Posting dates (monthly breakdown)

### Data Formats
1. **Flat File** (`job_postings_flat.csv`): 136 MB single table - *Not on GitHub*
2. **Monthly Excel** (`job_postings_monthly.xlsx`): Multi-sheet workbook
3. **Individual Monthly Files** (`monthly_files/`): 12 separate Excel files
4. **Star Schema** (`star_schema_files/`): Normalized relational structure

---

## 🎓 Learning Resources

### Official Documentation
- [Power BI Documentation](https://docs.microsoft.com/en-us/power-bi/)
- [DAX Function Reference](https://dax.guide/)
- [Power Query M Reference](https://docs.microsoft.com/en-us/powerquery-m/)

### Community
- [Power BI Community](https://community.powerbi.com/)
- [SQLBI (DAX experts)](https://www.sqlbi.com/)
- [Guy in a Cube (YouTube)](https://www.youtube.com/channel/UCFp1vaKzpfvoGai0vE5VJ0w)

---

## 🤝 Contributing

Found an error or want to suggest an improvement?

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -m 'Add some improvement'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Open a Pull Request

---

## 📝 Notes

### Why Median Over Average?
Throughout the salary analysis, I consistently used **median instead of average** because:
- Median is resistant to outliers (extremely high or low salaries)
- Provides a more realistic representation of typical compensation
- Better reflects the actual market conditions for most professionals
- Average can be skewed by a few executives or entry-level positions

### File Size Limitations
Some files exceed GitHub's 100 MB limit:
- `job_postings_flat.csv` (136.35 MB) - Tracked with Git LFS
- `job_postings_fact.csv` (75.33 MB) - Tracked with Git LFS
- Several large `.pbix` files - Tracked with Git LFS

If you need these files, ensure Git LFS is installed and run `git lfs pull`.

---

## 📜 License

This project is for educational purposes. Data used in this course is for demonstration and learning only.

---

## 👤 Author

**Cristian Ruse**
- GitHub: [@RuseCristian](https://github.com/RuseCristian)
- Repository: [power-bi-course](https://github.com/RuseCristian/power-bi-course)

---

## 🙏 Acknowledgments

Special thanks to the Power BI community and all the educators who make learning data analytics accessible to everyone.

---

⭐ **If you found this repository helpful, please consider giving it a star!** ⭐
