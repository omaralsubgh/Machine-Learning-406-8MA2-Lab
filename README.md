# ARTI406 - Machine Learning: Assignment 1
## Exploratory Data Analysis (EDA) on Chocolate Sales

### Project Overview
This project focuses on the most critical phase of any Machine Learning workflow: **Exploratory Data Analysis (EDA)**. Before building predictive models, we must understand the underlying patterns, anomalies, and relationships within the data. 

In this assignment, I perform a comprehensive EDA on a global Chocolate Sales dataset to derive business insights and prepare the data for future modeling.

---

### Dataset Description
The dataset used is `Chocolate_Sales.csv`, which contains transaction records including:
* **Sales Person**: The individual responsible for the sale.
* **Country**: The geographic location of the transaction.
* **Product**: The specific chocolate variety sold.
* **Date**: The transaction timestamp.
* **Amount**: The revenue generated (initially formatted as currency strings).
* **Boxes Shipped**: The volume of product moved.

---

### EDA Workflow

#### 1. Data Cleaning & Preprocessing
* **Library Imports**: Utilizing `pandas`, `numpy`, `matplotlib`, and `seaborn`.
* **Handling Duplicates**: Identified and removed redundant entries to ensure data integrity.
* **Missing Values**: Addressed null entries in geographic data.
* **Type Casting**: Converted `Amount` from string objects (removing `$` and `,`) to numerical floats and transformed `Date` into `datetime` objects for time-series analysis.

#### 2. Statistical Analysis
* Generated descriptive statistics to understand mean revenue, standard deviation, and the distribution of shipping volumes.

#### 3. Data Visualization
Key insights were visualized through:
* **Revenue by Sales Person**: Identifying top-performing employees.
* **Geographic Performance**: Mapping total revenue across different countries.
* **Monthly Sales Trends**: A time-series analysis to detect seasonality and growth.
* **Product Popularity**: Ranking products based on the total number of boxes shipped.

---

### Key Findings
* **Market Leaders**: India and Australia emerge as the highest revenue-generating regions.
* **Top Products**: Certain varieties like "70% Dark Bites" show significantly higher shipping volumes compared to others.
* **Performance**: Visual analysis highlights a small group of salespersons responsible for a majority of the total revenue.
