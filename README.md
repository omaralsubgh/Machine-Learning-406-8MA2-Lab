# Assignment 2: Data Quality Assessment & Preprocessing
**Course:** ARTI406 - Machine Learning  
**Student:** Omar Salman Alsubgh

---

## 📌 Project Overview
This notebook contains a complete data preprocessing pipeline applied to the **Smartphone Usage and Productivity** dataset. The goal is to clean, transform, and reduce the data to prepare it for machine learning analysis.

## 🛠 Preprocessing Pipeline

### 1. Data Quality Assessment
We verified the dataset for integrity. The data was found to be highly consistent with no initial missing values or duplicate records.

### 2. Handling Missing Values
To simulate a real-world scenario, missing values were manually introduced into the `Daily_Phone_Hours` column. 
* **Strategy:** Median Imputation.
* **Reasoning:** The median is used because it is robust against outliers, ensuring that the typical usage pattern is preserved without skewing the distribution.

### 3. Outlier Management
Outliers were detected using the **Interquartile Range (IQR)** method. 
* **Threshold:** A multiplier of `0.5` was used to identify and filter out extreme usage behaviors at the far ends of the distribution.

### 4. Feature Scaling (Normalization)
To ensure all features contribute equally to the model:
* **Min-Max Scaling:** Rescaled numerical data to a $[0, 1]$ range.
* **Z-Score Standardization:** Centered data around a mean of $0$ with a standard deviation of $1$. This is a prerequisite for PCA.

### 5. Dimensionality Reduction (PCA)
Principal Component Analysis was performed to observe behavioral patterns.
* **Finding:** Due to low correlation between features, the variance is spread across multiple components. 
* **Conclusion:** User behavior in this dataset is multi-dimensional and independent.

---
**Tools Used:** `Pandas`, `NumPy`, `Matplotlib`, `Seaborn`, `Scikit-Learn`