# 📊 E-Commerce Sales Analysis Using Python

## 📌 Project Overview

This project analyzes **e-commerce retail transactions** using Python to identify sales trends, top-performing products, customer purchasing behavior, revenue contribution, and country-wise performance.

The project uses **Pandas, NumPy, and Matplotlib** for data cleaning, exploratory data analysis (EDA), calculations, and visualization.

The complete analysis was performed using **Google Colab**.

---

## 🎯 Objectives

The main objectives of this project are:

* Clean and prepare raw retail transaction data
* Analyze total sales and quantity sold
* Calculate revenue and average unit price
* Identify top-performing products
* Analyze customer spending behavior
* Analyze country-wise sales performance
* Identify monthly, daily, and yearly sales trends
* Analyze cancelled transactions
* Calculate product and customer revenue contribution
* Create meaningful business visualizations
* Generate actionable business insights

---

## 📂 Dataset

**Dataset:** Online Retail II

The dataset contains historical transactions from an online retail business.

### Main Columns

| Column        | Description                   |
| ------------- | ----------------------------- |
| `Invoice`     | Invoice or transaction number |
| `StockCode`   | Product code                  |
| `Description` | Product description           |
| `Quantity`    | Number of items purchased     |
| `InvoiceDate` | Date and time of transaction  |
| `Price`       | Unit price of the product     |
| `Customer ID` | Unique customer identifier    |
| `Country`     | Customer's country            |

---

## 🛠️ Technologies Used

* **Python**
* **Google Colab**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Excel**

---

## 📦 Requirements

The following Python libraries are required:

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
```

For Excel file handling:

```text
openpyxl
```

### requirements.txt

```text
pandas
numpy
matplotlib
openpyxl
```

---

# 🔄 Project Workflow

```text
Raw Dataset
     ↓
Data Import
     ↓
Data Understanding
     ↓
Data Cleaning
     ↓
Feature Engineering
     ↓
Exploratory Data Analysis
     ↓
Product Analysis
     ↓
Customer Analysis
     ↓
Time Analysis
     ↓
Country Analysis
     ↓
Advanced Analysis
     ↓
Data Visualization
     ↓
Business Insights
```

---

# 🧹 Data Cleaning

The following data-cleaning steps were performed:

* Checked dataset shape
* Checked column names
* Checked data types
* Checked missing values
* Checked duplicate records
* Removed duplicate records
* Converted `InvoiceDate` to datetime
* Identified cancelled transactions
* Identified negative quantities
* Identified invalid prices
* Created a revenue column
* Created a cleaned sales dataset

### Revenue Calculation

```python
df['Revenue'] = df['Quantity'] * df['Price']
```

### Cancelled Transaction Identification

```python
df['Cancelled'] = df['Invoice'].astype(str).str.startswith('C')
```

### Valid Sales Dataset

```python
sales_df = df[
    (~df['Cancelled']) &
    (df['Quantity'] > 0) &
    (df['Price'] > 0)
].copy()
```

---

# 📊 Sales Analysis

The project analyzes:

* Total quantity sold
* Total revenue
* Average unit price
* Average order value
* Highest-value transaction
* Lowest-value transaction
* Most frequently sold product
* Product with highest quantity sold
* Product with highest revenue
* Top 10 products by revenue
* Bottom-performing products
* Product-wise revenue
* Product-wise quantity
* Product-wise average price
* Products generating above-average revenue
* Product revenue contribution
* Products with unusually high quantities
* Products with unusually high prices
* Product sales by country

---

# 👥 Customer Analysis

Customer-level analysis includes:

* Total customer spending
* Top spending customers
* Highest-spending customer
* Customers with the most orders
* Average customer spending
* Average number of orders
* Customers spending above average
* Customers with more than 10 orders
* One-time customers
* Repeat customers
* Customer revenue contribution
* Customer Average Order Value
* High-value customers
* Country-wise customer spending

---

# 📅 Time-Based Analysis

Sales trends are analyzed by:

* Year
* Month
* Day
* Weekday

The analysis includes:

* Monthly revenue
* Monthly quantity sold
* Monthly order count
* Best-performing month
* Worst-performing month
* Daily revenue
* Best sales day
* Worst sales day
* Average daily revenue
* Yearly revenue comparison
* Weekday revenue
* Monthly order trends

---

# 🌍 Country Analysis

Country-level analysis includes:

* Revenue by country
* Top countries by revenue
* Countries with the most orders
* Countries with the highest quantity sold
* Average Order Value by country
* Countries with above-average revenue
* Revenue contribution by country
* Customer count by country
* Average customer spending by country
* Customer count versus revenue

---

# 🚀 Advanced Analysis

Advanced analysis includes:

### Revenue Analysis

* Revenue calculation
* Product revenue ranking
* Customer revenue ranking
* Running monthly revenue
* Monthly revenue growth
* Percentage change
* 3-month moving average

### Customer Analysis

* Customer lifetime spending
* Repeat customers
* Purchase frequency
* Customer segmentation
* Top customers by country

### Product Analysis

* Product ranking
* Top 3 products by country
* Product revenue contribution
* Product quantity analysis

### Cancellation Analysis

* Cancelled transactions
* Cancellation rate
* Cancelled versus completed transactions
* Cancelled quantities
* Cancellation revenue impact

---

# 📈 Data Visualizations

The project includes visualizations such as:

* Monthly revenue
* Top 10 products by revenue
* Top 10 customers by revenue
* Revenue by country
* Quantity by product
* Daily revenue trend
* Monthly sales trend
* Customer spending distribution
* Quantity versus revenue
* Cancellation analysis

---

# 💡 Key Business Questions

This project answers questions such as:

1. Which products generate the highest revenue?
2. Which products sell the highest quantity?
3. Who are the highest-spending customers?
4. Which countries generate the most revenue?
5. Which month has the highest sales?
6. What is the average unit price?
7. What percentage of total revenue comes from each product?
8. How many transactions are cancelled?
9. Who are the repeat customers?
10. Is there a relationship between quantity and revenue?
11. Which products contribute most to overall revenue?
12. What are the major sales trends over time

---

# 📁 Project Structure

```text
Ecommerce-Sales-Analysis-Python/
│
├── README.md
├── Online_Retail_II_Analysis.ipynb
├── requirements.txt
│
├── dataset/
│   └── online_retail_II.xlsx
│
└── visualizations/
    ├── monthly_revenue.png
    ├── top_10_products.png
    ├── top_customers.png
    ├── revenue_by_country.png
    ├── quantity_by_product.png
    ├── daily_revenue.png
    ├── spending_distribution.png
    ├── quantity_vs_revenue.png
    └── cancellation_analysis.png
```

---

# ▶️ How to Run

## Google Colab

1. Open the project notebook in Google Colab.
2. Upload the `online_retail_II.xlsx` dataset.
3. Run the notebook cells from top to bottom.
4. Review the analysis results.
5. Review the generated visualizations.

## Local Environment

Install the required libraries:

```bash
pip install pandas numpy matplotlib openpyxl
```

Then open the Jupyter Notebook and run the cells.

---

# 🎓 Skills Demonstrated

This project demonstrates practical skills in:

* Python
* Pandas
* NumPy
* Data Cleaning
* Data Wrangling
* Exploratory Data Analysis
* GroupBy
* Aggregation
* Filtering
* Sorting
* Datetime Analysis
* Feature Engineering
* Product Analysis
* Customer Analysis
* Revenue Analysis
* Data Visualization
* Business Intelligence
* Business Insight Generation

---

# 💼 Portfolio Value

This project demonstrates the ability to take a raw e-commerce dataset and transform it into meaningful business information through:

**Data Cleaning → Analysis → Visualization → Business Insights**

It is suitable as a **Data Analyst portfolio project** and demonstrates practical Python-based data analysis skills.

---

# 👨‍💻 Author

**Anoop K S**

Aspiring Data Analyst

### Technical Skills

`Python` `SQL` `Excel` `Power BI` `Tableau` `Pandas` `NumPy` `Data Visualization`

---

## ⭐ Project Highlights

* 📊 E-commerce sales analysis
* 🧹 Data cleaning and preprocessing
* 📈 Revenue and product analysis
* 👥 Customer behavior analysis
* 🌍 Country-wise analysis
* 📅 Time-series analysis
* 📉 Cancellation analysis
* 📊 Data visualization
* 💡 Business insights

## 📌 Conclusion

This project demonstrates the use of **Python, Pandas, NumPy, and Matplotlib** to analyze e-commerce sales data, identify sales trends, understand customer and product performance, and generate meaningful business insights.

