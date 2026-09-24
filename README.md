# 🛒 Online Retail Sales Analysis

An end-to-end **Exploratory Data Analysis (EDA)** project using the **[UCI Online Retail Dataset](https://archive.ics.uci.edu/dataset/352/online+retail)**.  to analyze sales performance, customer behavior, product performance, returns, and revenue distribution across different countries.

The project was developed as part of the **Roadmap.sh E-commerce Data Analysis Project** and focuses on transforming raw transactional data into meaningful business insights through data cleaning, analysis, visualization, and interpretation.

---

## 📌 Project Overview

This project analyzes transactional data from a UK-based online retail business covering the period from **01/12/2010 to 09/12/2011**.

The dataset contains more than **500,000 real-world transactions** and includes common data-quality challenges such as:

* Missing values
* Inconsistent data types
* Cancelled invoices
* Returned products
* Zero-price transactions
* Negative quantities

A **10% sample** of the original dataset was used for the analysis.

The complete workflow follows:

**Raw Data → Sampling → Data Cleaning → Data Preparation → Revenue Calculation → EDA → Visualization → Insights → Business Recommendations**

---

## 🎯 Objectives

The main objectives of this project were to:

* Clean and prepare real-world transactional data.
* Calculate transaction-level revenue.
* Analyze sales performance over time.
* Examine revenue distribution across countries.
* Analyze customer purchasing behavior.
* Identify top-performing products.
* Identify returns and cancelled orders.
* Create informative data visualizations.
* Translate analytical findings into actionable business recommendations.

---

## 📊 Dataset Information

The analysis is based on the **UCI Online Retail Dataset**.

| Detail        | Value                           |
| ------------- | ------------------------------- |
| Dataset       | UCI Online Retail Dataset       |
| Source        | UCI Machine Learning Repository |
| Original Rows | 541,909                         |
| Features      | 8                               |
| Business Type | UK-based Online Retail          |
| Period        | 01/12/2010 – 09/12/2011         |
| Sample Used   | 10% of the original dataset     |

### 🔗 Dataset Source

[UCI Online Retail Dataset](https://archive.ics.uci.edu/dataset/352/online+retail)

---

## 🧬 Dataset Features

| Column        | Description                                    |
| ------------- | ---------------------------------------------- |
| `InvoiceNo`   | Unique identifier for each invoice/transaction |
| `StockCode`   | Unique identifier for each product             |
| `Description` | Product name or description                    |
| `Quantity`    | Number of units purchased                      |
| `InvoiceDate` | Date and time of the transaction               |
| `UnitPrice`   | Price per unit                                 |
| `CustomerID`  | Unique identifier for each customer            |
| `Country`     | Customer's country                             |

---

## 🧹 Data Cleaning & Preparation

Several data-cleaning steps were performed before the analysis:

### Missing Values

Missing values were identified and handled according to their relevance to the analysis.

### Data Types

Columns were converted to appropriate data types, including:

* `InvoiceDate` → `datetime`
* Numerical fields → appropriate numeric types

### Returns

Transactions containing negative `Quantity` values were identified as product returns.

### Cancelled Orders

Cancelled invoices were identified using the invoice information provided in the dataset.

### Zero-Price Transactions

Transactions with a `UnitPrice` of zero were identified and considered during data preparation.

The objective of the cleaning stage was to create a reliable dataset for revenue and sales analysis while preserving the original transactional information required for the study.

---

## 💰 Revenue Calculation

A new `Revenue` feature was calculated at the transaction level:

```text
Revenue = Quantity × UnitPrice
```

This derived metric was used throughout the analysis to evaluate:

* Total revenue
* Revenue by country
* Monthly revenue
* Product revenue
* Customer revenue
* Revenue concentration

---

## 🔍 Exploratory Data Analysis

The analysis explored several dimensions of the retail business.

### Sales Performance

* Total revenue
* Total orders
* Monthly revenue
* Monthly order volume
* Average revenue per customer

### Geographic Analysis

* Revenue by country
* Orders by country
* Revenue concentration across countries

### Product Analysis

* Top products by quantity sold
* Top products by revenue
* Product revenue contribution
* Comparison between product popularity and revenue performance

### Customer Analysis

* Unique customers
* Customer revenue
* High-value customers
* Revenue concentration among customers

### Returns & Cancellations

* Returned quantities
* Return rate
* Cancelled invoices
* Impact of returns on sales performance

---

## 📈 Key Performance Metrics

The following metrics were obtained from the **10% sample used in this analysis**:

| Metric                               |         Value |
| ------------------------------------ | ------------: |
| Total Revenue                        | 9,726,006.954 |
| Total Orders                         |        24,446 |
| Unique Customers                     |         4,372 |
| Highest Revenue Month                | November 2011 |
| November 2011 Revenue                |       ≈ 1.46M |
| Top 5 Countries Revenue Contribution |      ≈ 93.91% |
| Return Rate                          |       ≈ 1.82% |
| Average Revenue per Customer         |    ≈ 1,893.53 |
| Top 10 Products Revenue Contribution |      ≈ 10.86% |

> **Note:** These metrics represent the analyzed sample and should not be interpreted as full-dataset totals.

---

## 📊 Data Visualization

The analysis uses **Matplotlib** and **Seaborn** to visualize the main patterns and relationships within the dataset.

The visualizations cover:

* Monthly revenue trends
* Monthly order trends
* Revenue by country
* Orders by country
* Top products by quantity
* Top products by revenue
* Customer revenue distribution
* Return analysis
* Revenue concentration

Visualizations are stored in:

```text
images/
└── visualizations/
```

---

## 💡 Key Insights

### 🌍 Geographic Performance

The **United Kingdom generates the majority of the revenue**, highlighting the importance of the domestic market within the analyzed transactions.

A relatively small number of countries account for most of the revenue, with the **top five countries contributing approximately 93.91%** of the analyzed revenue.

### 📅 Monthly Performance

**November 2011** recorded the highest monthly revenue, reaching approximately **1.46M** in the analyzed sample.

This indicates a significant increase in sales activity during that period.

### 👥 Customer Behavior

Revenue is not distributed evenly across customers.

A relatively small group of customers contributes a substantial share of total revenue, indicating the importance of understanding and retaining high-value customers.

### 📦 Product Performance

Product popularity and revenue performance are not always the same.

Some products may have high quantities sold while contributing less revenue, while other products can generate substantial revenue despite lower sales volume.

### 🔄 Returns

Returns represent approximately **1.82%** of the analyzed transactions according to the project's return-rate calculation.

Monitoring returned products can help identify potential issues related to product demand, quality, customer expectations, or purchasing patterns.

---

## 🚀 Business Recommendations

Based on the analytical findings, several business actions can be considered:

### 1. Focus on High-Performing Markets

Use country-level revenue analysis to prioritize marketing, customer retention, and sales strategies in markets generating the largest share of revenue.

### 2. Develop High-Value Customer Strategies

Identify customers with consistently high revenue contribution and consider targeted retention and loyalty strategies.

### 3. Promote High-Revenue Products

Product strategies should consider **revenue contribution**, not only quantity sold.

### 4. Monitor Returned Products

Products with unusually high return volumes can be investigated to identify potential issues in product quality, descriptions, pricing, or customer expectations.

### 5. Use Seasonal Sales Patterns

Monthly revenue trends can support:

* Inventory planning
* Promotional campaigns
* Sales forecasting
* Resource allocation

### 6. Evaluate Products Using Multiple Metrics

Product performance should be evaluated using both:

* Quantity sold
* Revenue generated

This provides a more complete view of product performance.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Jupyter Notebook**

---

## 📁 Project Structure

```text
Online-Retail-Sales-Analysis/
│
├── Online Retail.xlsx
├── Online_Retail_Analysis.ipynb
├── README.md
│
└── images/
    └── visualizations/
```

---

## 📚 What I Learned

This project strengthened my understanding of the complete **data analysis workflow**, from working with raw transactional data to communicating analytical findings.

Through this project, I practiced:

* Data cleaning and preprocessing
* Handling missing and inconsistent data
* Working with datetime data
* Feature engineering
* Revenue calculation
* Exploratory Data Analysis
* Grouping and aggregation with Pandas
* Data visualization
* Customer and product analysis
* Geographic analysis
* Translating analytical results into business insights

Most importantly, the project helped me understand how raw transactional data can be transformed into information that supports data-driven business decisions.

---

## ✅ Conclusion

The analysis of the UCI Online Retail Dataset demonstrates how real-world transactional data can be transformed into meaningful business insights.

The analysis identified important patterns in:

* Revenue distribution
* Geographic performance
* Monthly sales
* Customer behavior
* Product performance
* Returns and cancellations

The findings provide a foundation for further analysis such as **customer segmentation, RFM analysis, sales forecasting, market basket analysis, and predictive modeling**.

---

## 👩‍💻 Author

### Noura Maher Elamin

Data Analysis & Machine Learning Enthusiast

### Connect With Me

* **LinkedIn:** [Noura Maher Elamin](https://www.linkedin.com/in/nouramaherelamin/)
* **GitHub:** [Noura Maher Elamin](https://github.com/nouramaherelamin)

---

<div align="center">

⭐ **If you find this project useful, consider giving the repository a star!**

</div>
