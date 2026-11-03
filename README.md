# 🚀 E-Commerce Data Analytics Pipeline (Project 1, 2 & 3) 📊

## 📌 Project Overview 🌟
This project is an end-to-end Data Analytics pipeline built for the DecodeLabs Internship. It processes raw e-commerce data to ensure data integrity, uncovers hidden business patterns through Exploratory Data Analysis (EDA), and executes advanced SQL queries to extract actionable business intelligence. 🧠💡

## 🛠️ Tools & Technologies Used 💻
* **Python** 🐍 (Core Logic)
* **Pandas** 🐼 (Data Cleaning, Aggregation & EDA)
* **NumPy** 🔢 (Mathematical Operations)
* **SQLite3 & SQL** 🗄️ (Database Management & Execution Engine)
* **Google Colab** ☁️ (Execution Environment)

## 🔍 Key Phases Completed 🏆

### 🧹 Phase 1: Data Cleaning (The Foundation)
* **Duplicate Removal:** Enforced the strict "One Truth, One Record" rule. ✅
* **Missing Value Imputation:** Handled `NaN` values in the `CouponCode` column by replacing them with "No Coupon" to preserve 100% data volume without dropping any rows. 🛡️
* **Structural Integrity:** Reset the index to maintain perfect sequential order. 🔢

### 📈 Phase 2: Exploratory Data Analysis (EDA)
* **Statistical Summary 🩻:** Evaluated central tendencies using `df.describe()`. Discovered significant right-skewness in the `TotalPrice` column (Mean vs Median gap).
* **Outlier Detection (IQR Method) 🚨:** Mathematically identified **8 high-value transactions** (VIP/Bulk orders) that bypassed the upper safe limit (3330.40). These were flagged for business review, not deleted! 👑
* **Correlation Analysis 🤝:** Used `df.corr()` to map variable relationships. Confirmed a strong positive correlation **(0.71)** between `UnitPrice` and `TotalPrice`. 💸

### 🗄️ Phase 3: SQL Data Analysis (The Execution Engine)
* **Virtual Database Creation 🔌:** Transferred cleaned Excel data into a live SQLite database using Pandas `to_sql`.
* **Precision Filtering 🌪️:** Used the `WHERE` clause to strictly isolate 'Delivered' orders.
* **Data Aggregation & Grouping 🪣:** Grouped data by `Product` and applied the `SUM()` function to calculate Total Sales.
* **Actionable Insights 🥇:** Sorted results using `ORDER BY DESC` to successfully identify the highest revenue-generating products (e.g., Laptops & Phones).

## 🚀 How to Run This Project ⚙️
1. Clone this repository to your local machine or open it directly in Google Colab. 🌐
2. Ensure you have the dataset: `Dataset for Data Analytics.xlsx` in the same directory. 📁
3. Install the required VIP libraries: `pip install pandas numpy openpyxl` 📦
4. Run all cells in the respective Google Colab notebooks to view the complete pipeline from cleaning to SQL execution! 🔥
