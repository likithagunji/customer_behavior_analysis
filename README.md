# customer_behavior_analysis
Data Analytics project showcasing customer behavior analysis using python, sql and power BI
# Data Analytics Project

## Overview

This project demonstrates an end-to-end **Data Analytics workflow**, starting from data loading and exploratory analysis to SQL analysis, data visualization, reporting, and presentation.

The project uses **Python for data analysis and cleaning, PostgreSQL for SQL-based analysis, and Power BI for interactive dashboard development**. A final project report and presentation were also created to communicate the key findings.

---

## Dataset

The project uses a structured dataset containing customer and transaction-related information.

The dataset was initially loaded into Python for:

* Data exploration
* Data quality checks
* Missing-value analysis
* Duplicate detection
* Data cleaning and transformation
* Feature creation
* Exploratory Data Analysis (EDA)

---

## Tools & Technologies

| Tool                    | Purpose                                         |
| ----------------------- | ----------------------------------------------- |
| **Python**              | Data loading, cleaning, transformation, and EDA |
| **Pandas**              | Data manipulation and analysis                  |
| **NumPy**               | Numerical operations                            |
| **Jupyter Notebook**    | Python-based analysis                           |
| **PostgreSQL**          | SQL querying and database analysis              |
| **SQLAlchemy**          | Connecting Python with PostgreSQL               |
| **Power BI**            | Dashboard and data visualization                |
| **Gamma**               | Project presentation                            |
| **Microsoft Excel/CSV** | Dataset handling and supporting analysis        |

---

## Project Workflow

### 1. Data Loading

The dataset was imported into Python using Pandas.

```python
import pandas as pd

df = pd.read_csv("dataset.csv")
```

Initial checks were performed to understand the dataset structure:

```python
df.head()
df.shape
df.info()
df.describe()
```

### 2. Exploratory Data Analysis (EDA)

EDA was performed to understand patterns, distributions, and relationships within the data.

Key activities included:

* Understanding numerical and categorical variables
* Analyzing distributions
* Checking unique values
* Identifying missing values
* Detecting duplicate records
* Identifying potential outliers
* Studying relationships between variables

### 3. Data Cleaning

The dataset was prepared for analysis by:

* Handling missing values
* Removing duplicate records
* Correcting data types
* Standardizing column names
* Validating inconsistent values
* Creating derived columns where required

Example:

```python
df.isnull().sum()
df.duplicated().sum()
```

### 4. Feature Engineering

Additional analytical columns were created where required.

For example, customer ages were categorized into groups:

```python
labels = ['Young Adult', 'Adult', 'Middle-aged', 'Senior']

df['age_group'] = pd.qcut(
    df['age'],
    q=4,
    labels=labels
)
```

### 5. PostgreSQL & SQL Analysis

The cleaned dataset was loaded into a **PostgreSQL database**.

Python and PostgreSQL were connected using SQLAlchemy.

SQL queries were then used to perform analytical tasks such as:

* Aggregations
* Filtering
* Grouping
* Sorting
* Customer analysis
* Sales analysis
* Category-level analysis
* Business performance analysis

Example:

```sql
SELECT
    category,
    SUM(sales) AS total_sales
FROM customer_data
GROUP BY category
ORDER BY total_sales DESC;
```

### 6. Power BI Dashboard

The analyzed data was connected to **Power BI** to create an interactive dashboard.

The dashboard focuses on presenting important business metrics and trends through:

* KPI cards
* Charts
* Category analysis
* Customer analysis
* Sales/transaction trends
* Interactive filters and slicers

The dashboard enables users to explore the data and identify important patterns more easily.

---

## Dashboard

The Power BI dashboard provides an interactive view of the analyzed data.

### Key Dashboard Components

* **KPI Metrics** – High-level business performance indicators
* **Trend Analysis** – Changes over time
* **Category Analysis** – Comparison across different categories
* **Customer Analysis** – Customer-related insights
* **Interactive Filters** – Dynamic exploration of the dataset

> Add your Power BI dashboard screenshot here.

```text
![Power BI Dashboard](images/dashboard.png)
```

---

## Results & Insights

The analysis helped identify important patterns and trends within the dataset.

Key outcomes included:

* Identification of major customer and transaction patterns
* Analysis of category-level performance
* Understanding of customer age-group distribution
* Identification of data-quality issues
* SQL-based analysis of business metrics
* Development of an interactive dashboard for decision-making

The project demonstrates how raw data can be transformed into **structured insights and business-friendly visualizations**.

---

## Project Report

A detailed project report was prepared covering:

1. Business/Project Objective
2. Dataset Description
3. Data Cleaning
4. Exploratory Data Analysis
5. SQL Analysis
6. Power BI Dashboard
7. Key Findings
8. Conclusion

---

## Presentation

A presentation was created using **Gamma** to communicate the project workflow, analysis, dashboard, and key findings in a concise format.

---

## Project Structure

```text
Data-Analytics-Project/
│
├── data/
│   └── dataset.csv
│
├── notebooks/
│   └── data_analysis.ipynb
│
├── sql/
│   └── analysis_queries.sql
│
├── powerbi/
│   └── dashboard.pbix
│
├── report/
│   └── project_report.pdf
│
├── presentation/
│   └── project_presentation.pdf
│
├── images/
│   └── dashboard.png
│
└── README.md
```

---

## How to Run

### 1. Clone the Repository

```bash
git clone <repository-url>
cd Data-Analytics-Project
```

### 2. Install Python Libraries

```bash
pip install pandas numpy sqlalchemy psycopg2-binary matplotlib seaborn
```

### 3. Run the Jupyter Notebook

Open:

```bash
jupyter notebook
```

Then run the notebook:

```text
notebooks/data_analysis.ipynb
```

### 4. Set Up PostgreSQL

Create a PostgreSQL database and update the database connection details in the Python script/notebook.

Example:

```python
from sqlalchemy import create_engine

engine = create_engine(
    "postgresql+psycopg2://username:password@localhost:5432/database_name"
)
```

Run the SQL queries from:

```text
sql/analysis_queries.sql
```

### 5. Open the Power BI Dashboard

Open:

```text
powerbi/dashboard.pbix
```



---

## Skills Demonstrated

* **Python**
* **Pandas & NumPy**
* **Exploratory Data Analysis**
* **Data Cleaning**
* **Feature Engineering**
* **SQL**
* **PostgreSQL**
* **Database Connectivity**
* **Power BI**
* **Data Visualization**
* **Business Intelligence**
* **Data Storytelling**
* **Reporting & Presentation**

---

## Conclusion

This project demonstrates an end-to-end approach to data analytics, from **raw data preparation to extracting insights and presenting them through interactive dashboards and reports**.

