# 🛒 Data Cleaning & EDA: Online Retail Sales

This project analyzes and cleans the **UCI Online Retail Dataset**, a real-world transactional dataset from a UK-based e-commerce business. The goal is to assess and improve data quality, and extract actionable insights through exploratory data analysis (EDA).

## 📁 Dataset

- **Source**: [UCI Machine Learning Repository – Online Retail Dataset](https://archive.ics.uci.edu/ml/datasets/Online+Retail)
- **File**: `Online Retail.xlsx`
- **Size**: ~540,000 rows
- **Fields**:  
  - `InvoiceNo`: Unique invoice number  
  - `StockCode`: Product/item identifier  
  - `Description`: Product name  
  - `Quantity`: Number of items purchased  
  - `InvoiceDate`: Date and time of transaction  
  - `UnitPrice`: Price per item (GBP)  
  - `CustomerID`: Customer identifier  
  - `Country`: Country of purchase

## 🧰 Technologies Used

- **Python 3**
- **Pandas** – data cleaning and manipulation  
- **Matplotlib / Seaborn** – data visualization  
- **Jupyter Notebook / Google Colab** – interactive analysis

## 🔍 Workflow Summary

1. **Data Inspection**
   - Initial data profiling and statistical summary
   - Identified missing values and data types

2. **Data Cleaning**
   - Removed **5,268 duplicate records**
   - Removed **2,517 invalid price entries** (`UnitPrice <= 0`)
   - Dropped transactions with **negative quantity values**
   - Imputed missing `CustomerID` values as `'Unknown'`

3. **Feature Engineering**
   - Created a `Revenue` column as `Quantity × UnitPrice`

4. **Exploratory Data Analysis**
   - Top-selling products by quantity
   - Number of transactions by country
   - Revenue by country
   - Unit price distribution
   - Monthly revenue trends
   - Correlation heatmap between numerical variables

## 📈 Key Insights

- **The UK dominates** the market, with over 90% of all transactions.
- The dataset had major data quality issues: **duplicate rows, invalid prices, and missing customer identifiers**.
- **Top-selling products** are seasonal or giftable items like *Paper Craft* and *Little Birdie*.
- **Revenue is concentrated** in a small number of countries.
- **Monthly revenue trends** reveal growth approaching year-end, indicating seasonality.

## 💡 Recommendations

- Enforce **data validation** during entry to prevent invalid pricing and quantities.
- Ensure **CustomerID is consistently captured**, even for single-time purchases.
- Monitor **high-performing products** for inventory planning and marketing focus.
- Leverage **seasonal peaks** for campaign planning and product promotions.

## 📌 Conclusion

This project cleaned and prepared the Online Retail dataset for future use in modeling and analytics. Through effective data profiling and EDA, key business insights were identified to support marketing, inventory, and customer experience decisions. This type of foundational work is essential before moving on to more advanced tasks like segmentation, forecasting, or recommender systems.

## 📎 Files Included

- `data_cleaning_eda_online_retail_sales_data.py` – Full code script (auto-exported from Colab)
- `Online Retail.xlsx` – Original dataset (must be downloaded manually)
- `README.md` – Project overview and documentation