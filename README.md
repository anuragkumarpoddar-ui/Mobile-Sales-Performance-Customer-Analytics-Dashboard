# 📱 Mobile Sales Performance & Customer Analytics Dashboard

<p align="center">
  <img src="https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black"/>
  <img src="https://img.shields.io/badge/DAX-512BD4?style=for-the-badge&logo=powerbi&logoColor=white"/>
  <img src="https://img.shields.io/badge/Power%20Query-1170B7?style=for-the-badge&logo=powerbi&logoColor=white"/>
  <img src="https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white"/>
  <img src="https://img.shields.io/badge/Data%20Cleaning-4B5563?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Data%20Visualization-6366F1?style=for-the-badge"/>
</p>

<p align="center">
  <b>Interactive Power BI dashboard for analyzing mobile sales performance, product trends, customer behavior, payment preferences, and geographic sales patterns.</b>
</p>

---

## 📊 Project Overview

The **Mobile Sales Performance & Customer Analytics Dashboard** is an interactive Power BI business intelligence project designed to analyze mobile sales transactions across different brands, models, cities, payment methods, customer ratings, and time periods.

The project focuses on transforming raw transaction-level data into meaningful business insights through:

* Data cleaning and validation
* Data transformation using Power Query
* DAX-based KPI development
* Interactive data visualization
* Product and brand performance analysis
* Geographic sales analysis
* Customer behavior analysis
* Time-based sales analysis

The dashboard provides a consolidated view of sales performance and customer purchasing patterns, helping businesses identify high-performing products, brands, locations, payment preferences, and customer trends.

---

## 🎯 Business Objective

The primary objective of this project is to answer:

> **How are mobile sales performing across products, brands, locations, customers, payment methods, and time periods?**

The analysis helps identify:

* Top-performing mobile brands
* Best-selling mobile models
* High-performing cities
* Customer purchasing behavior
* Preferred payment methods
* Customer rating patterns
* Sales trends over time
* Day-of-week sales patterns

---

## 🗂️ Dataset

The dataset contains **3,835 mobile sales transactions** covering the period **2021–2024**.

### Dataset Coverage

| Category                  | Details   |
| ------------------------- | --------- |
| 📦 Transactions           | 3,835     |
| 📅 Time Period            | 2021–2024 |
| 📱 Mobile Brands          | 5         |
| 📲 Mobile Models          | 15        |
| 🌍 Cities                 | 19        |
| 💳 Payment Methods        | 4         |
| 👥 Customer Data          | Included  |
| ⭐ Customer Ratings        | Included  |
| 💰 Sales Information      | Included  |
| 🧾 Transaction-Level Data | Included  |

### Key Data Attributes

The dataset includes information related to:

* Transaction ID
* Date
* Brand
* Mobile Model
* City
* Customer information
* Payment Method
* Units Sold
* Price Per Unit
* Customer Rating
* Day Name
* Sales/transaction information

---

# 🧹 Data Cleaning & Preparation

Data quality is an important part of this project. Before building the dashboard, the dataset was reviewed, cleaned, validated, and prepared for analysis.

## Data Cleaning

The following data-quality checks were performed:

* ✅ Checked dataset structure and data types
* ✅ Validated Transaction ID uniqueness
* ✅ Checked for duplicate records
* ✅ Checked missing/null values
* ✅ Standardized categorical values
* ✅ Validated numerical fields such as **Units Sold** and **Price Per Unit**
* ✅ Reviewed date-related fields
* ✅ Standardized inconsistent **Day Name** values
* ✅ Validated data consistency across relevant fields
* ✅ Prepared the final dataset for Power BI analysis

## Data Transformation

Using **Power Query / Power BI**, the data was transformed and prepared for dashboard development.

Key activities included:

* Cleaning and transforming source data
* Standardizing data types
* Preparing fields for visualization
* Validating analytical fields
* Creating business-ready metrics
* Organizing sales attributes for KPI reporting
* Creating DAX measures for analysis

---

# 🧮 DAX Measures

DAX was used to create the key business metrics displayed throughout the dashboard.

## 💰 Total Sales

```DAX
Total Sales =
SUMX(
    Sales_Data,
    Sales_Data[Units Sold] * Sales_Data[Price Per Unit]
)
```

Calculates total sales value using units sold and price per unit.

---

## 📦 Total Quantity

```DAX
Total Quantity =
SUM(Sales_Data[Units Sold])
```

Calculates the total number of mobile units sold.

---

## 🧾 Transactions

```DAX
Transactions =
COUNTROWS(Sales_Data)
```

Calculates the total number of sales transactions.

---

## 💵 Average Price

```DAX
Average =
AVERAGE(Sales_Data[Price Per Unit])
```

Calculates the average price per mobile unit.

---

# 📈 Dashboard Components

The dashboard combines multiple visualizations and interactive filters to provide a complete view of mobile sales performance.

## 1. 📌 KPI Cards

The dashboard provides high-level KPIs for quick performance monitoring:

* **Total Sales**
* **Total Quantity**
* **Transactions**
* **Average Price**

These KPIs provide an immediate overview of the overall sales performance.

---

## 2. 📈 Sales Trend Analysis

The sales trend visualization analyzes sales activity across time.

It helps identify:

* Changes in sales performance
* High and low sales periods
* Overall sales movement
* Potential time-based patterns

---

## 3. 🌍 Geographic Sales Analysis

The geographic analysis compares sales performance across different cities.

This helps identify:

* Top-performing cities
* Sales concentration
* Geographic differences in demand
* Potential high-value markets

---

## 4. 🏷️ Brand Performance Analysis

The brand analysis compares the performance of the five mobile brands using:

* Sales
* Quantity
* Transactions

This helps identify which brands contribute most to overall business performance.

---

## 5. 📱 Mobile Model Analysis

The mobile model analysis identifies the models contributing most to total sales.

It helps answer:

* Which models generate the highest sales?
* Which models have higher sales volume?
* Which products are driving overall performance?

---

## 6. 💳 Payment Method Analysis

The dashboard analyzes transactions across four payment methods:

* UPI
* Debit Card
* Credit Card
* Cash

This provides insight into customer payment preferences.

---

## 7. ⭐ Customer Rating Analysis

Customer ratings are analyzed to understand the distribution of customer satisfaction across the dataset.

This can help identify:

* Rating distribution
* Common customer rating levels
* Potential differences in customer experience across products

---

## 8. 📅 Day-of-Week Analysis

Sales activity is analyzed by day name to identify day-level purchasing patterns.

This helps answer:

* Which days generate higher sales?
* Which days have higher transaction activity?
* Are there noticeable differences between weekdays?

---

# 🎛️ Interactive Filters

The dashboard includes interactive filters that allow users to dynamically analyze the data.

Users can filter the dashboard by:

* 🏷️ Brand
* 📱 Mobile Model
* 💳 Payment Method
* 📅 Day Name

These filters allow users to drill down into specific segments and explore the data interactively.


---
# ❓ Business Questions & Key Findings

The dashboard was designed to answer practical business questions and translate transactional sales data into actionable insights rather than simply presenting visualizations.

## 💰 Sales Performance

### What is the overall sales performance?

The dashboard provides a consolidated view of total sales, total quantity sold, transaction volume, and average selling price, allowing stakeholders to quickly assess overall business performance.

### How many mobile units were sold?

The **Total Quantity** KPI measures the overall number of mobile units sold across all transactions and provides an overview of sales volume.

### How many transactions occurred?

The **Transactions** KPI tracks the total number of sales transactions, helping measure customer purchase activity and overall transaction volume.

### What is the average selling price?

The **Average Price** KPI calculates the average price per mobile unit, providing an indication of the overall pricing level across the analyzed transactions.

---

## 📱 Product Performance

### Which mobile brand generates the highest sales?

**Apple recorded the highest overall sales value at approximately ₹161.6M**, followed by Samsung at approximately ₹160.0M.

This indicates that Apple was the strongest-performing brand by sales value among the five brands analyzed.

### Which mobile models perform best?

The mobile model analysis enables identification of the models contributing the most to total sales and quantity, helping distinguish high-performing products from lower-performing models.

### Which brands generate the highest sales quantity?

Brand-level quantity analysis allows businesses to compare sales volume across brands and understand whether higher revenue is driven by greater unit volume or higher-priced products.

### Which products contribute most to overall revenue?

The model and brand performance analysis highlights the products contributing most to total sales, helping identify key revenue-generating products that may deserve greater business focus.

---

## 🌍 Geographic Performance

### Which cities contribute the most revenue?

**Delhi emerged as the strongest-performing city, generating approximately ₹203.9M in sales**, followed by Mumbai at approximately ₹127.2M.

This indicates a significant difference in sales contribution across cities.

### Where are sales concentrated geographically?

Sales are **geographically concentrated**, with Delhi and Mumbai contributing substantially more sales than several other cities in the dataset.

This highlights the importance of geographic segmentation when evaluating market performance.

### Which locations represent stronger sales markets?

Delhi and Mumbai stand out as the strongest sales markets in the analyzed dataset, indicating potentially higher customer demand and stronger market activity in these locations.

---

## 👥 Customer Behavior

### Which payment method is most frequently used?

**UPI recorded the highest transaction volume with approximately 1,011 transactions**, followed by Debit Card (948), Credit Card (947), and Cash (929).

This indicates that UPI was the most frequently used payment method in the dataset.

### What is the distribution of customer ratings?

The customer rating analysis provides a view of rating distribution across transactions, helping identify the most common customer rating levels and overall customer feedback patterns.

### Are there noticeable differences in purchasing behavior across products?

The dashboard allows users to compare product performance, transaction activity, payment methods, and customer ratings across different brands and models. These comparisons help identify variations in customer purchasing behavior across products.

---

## 📅 Time Analysis

### How does sales activity change over time?

The sales trend analysis provides a time-based view of sales activity from **2021 to 2024**, allowing stakeholders to identify changes, peaks, and lower-activity periods across the analyzed timeframe.

### Which days generate higher sales?

The day-of-week analysis compares sales activity across different days and helps identify days with relatively higher or lower sales and transaction activity.

### Are there identifiable sales patterns across different periods?

The time-based visualizations provide a foundation for identifying recurring sales patterns, changes in demand, and periods of higher or lower activity. These patterns can support further investigation into seasonality and customer purchasing trends.

---

## 💡 Overall Business Takeaways

The analysis highlights three key findings:

- 🏆 **Apple** was the highest-performing brand by sales value, with approximately **₹161.6M** in sales.
- 🌆 **Delhi** was the strongest-performing city, generating approximately **₹203.9M** in sales.
- 💳 **UPI** was the most frequently used payment method, accounting for approximately **1,011 transactions**.

These findings demonstrate how the dashboard can help stakeholders move from **raw transactional data to measurable business insights** across product, geographic, customer, and time dimensions.

# 🔍 Key Business Insights

The analysis generated several notable findings from the dataset.

## 🏆 Brand Performance

**Apple recorded the highest overall sales value** among the five analyzed brands, followed by Samsung.

Approximate sales:

| Brand      | Approx. Sales |
| ---------- | ------------: |
| 🥇 Apple   |       ₹161.6M |
| 🥈 Samsung |       ₹160.0M |
| OnePlus    |       ₹153.7M |
| Vivo       |       ₹150.1M |
| Xiaomi     |       ₹143.8M |

### Insight

> **Apple recorded the highest overall sales value among the analyzed brands, while Xiaomi recorded the lowest among the five brands.**

The relatively close sales values across the brands also indicate that sales performance is distributed across multiple brands rather than being dominated by a single brand.

---

## 🌆 Geographic Performance

**Delhi** was the strongest city in terms of sales.

| City      | Approx. Sales |
| --------- | ------------: |
| 🥇 Delhi  |       ₹203.9M |
| 🥈 Mumbai |       ₹127.2M |

### Insight

> **Sales are geographically concentrated, with Delhi and Mumbai contributing substantially more sales than other cities in the dataset.**

This highlights the importance of geographic segmentation when evaluating mobile sales performance.

---

## 💳 Payment Behavior

**UPI** recorded the highest number of transactions among the four payment methods.

| Payment Method | Approx. Transactions |
| -------------- | -------------------: |
| 🥇 UPI         |                1,011 |
| Debit Card     |                  948 |
| Credit Card    |                  947 |
| Cash           |                  929 |

### Insight

> **UPI is the most frequently used payment method in the dataset, indicating strong adoption of digital payments among customers.**

---

# 🛠️ Tools & Technologies

### Power BI

Used for:

* Interactive dashboard development
* KPI visualization
* Data exploration
* Geographic analysis
* Interactive filtering
* Business intelligence reporting

### DAX

Used for:

* Total Sales
* Total Quantity
* Transactions
* Average Price
* Business metric calculations

### Power Query

Used for:

* Data cleaning
* Data transformation
* Data validation
* Data preparation

### Excel

Used as part of the source-data preparation and analytical workflow.

---

# 🔄 Project Workflow

```text
Raw Sales Data
      │
      ▼
Data Inspection
      │
      ▼
Data Cleaning & Validation
      │
      ▼
Power Query Transformation
      │
      ▼
Data Preparation
      │
      ▼
DAX Measures
      │
      ▼
Power BI Data Visualization
      │
      ▼
Interactive Dashboard
      │
      ▼
Business Insights
```

---

# 📊 Dashboard Preview

<img width="1324" height="742" alt="Mobile Sales Performance   Customer Analytics Dashboard" src="https://github.com/user-attachments/assets/0e5b6e36-4891-4723-8395-3d24b9a87e1b" />



### GitHub Repository Structure

```text
Mobile-Sales-Performance-Customer-Analytics/
│
├── 📁 Dashboard/
│   └── Mobile_Sales_Dashboard.pbix
│
├── 📁 Dataset/
│   └── Mobile_Sales_Data.xlsx
│
├── 📁 Images/
│   └── mobile-sales-dashboard.png
│
├── 📁 Documentation/
│   └── Project_Documentation.pdf
│
└── README.md
```

---

# 💡 Skills Demonstrated

This project demonstrates practical skills in:

* 📊 Business Intelligence
* 📈 Data Visualization
* 🧹 Data Cleaning
* 🔄 Data Transformation
* 🧮 DAX
* ⚡ Power Query
* 📊 Power BI Dashboard Development
* 📑 Excel
* 📍 Geographic Analysis
* 👥 Customer Analytics
* 📱 Product Performance Analysis
* 💰 Sales Analytics
* 📅 Time-Based Analysis
* 💼 Business Problem Solving
* 🔎 Exploratory Data Analysis

---

# 🚀 Project Outcomes

Through this project, raw mobile sales transactions were transformed into an interactive business intelligence dashboard capable of providing insights into:

* Overall sales performance
* Brand-level performance
* Product-level performance
* Geographic sales distribution
* Customer payment behavior
* Customer ratings
* Day-of-week patterns
* Transaction activity

The project demonstrates how **data cleaning, transformation, DAX, and visualization can be combined to convert raw transactional data into actionable business insights.**

---


## 📌 Conclusion

The **Mobile Sales Performance & Customer Analytics Dashboard** provides a comprehensive view of sales performance across brands, mobile models, cities, payment methods, customer ratings, and time periods. By transforming and validating **3,835 transaction records** and applying **Power Query, DAX, and interactive Power BI visualizations**, the project converts raw sales data into meaningful business insights.

The analysis indicates that **Apple generated the highest overall sales value**, while **Delhi emerged as the strongest-performing city**, highlighting significant geographic concentration in sales. Among payment methods, **UPI recorded the highest transaction volume**, reflecting a strong preference for digital payments within the analyzed dataset. The dashboard also enables comparison of brand and model performance, customer ratings, and day-level sales activity to identify variations in customer behavior and sales patterns.

Overall, the project demonstrates how **data cleaning, transformation, analytical modeling, DAX, and business intelligence visualization** can be combined to support data-driven decision-making. The dashboard can help business stakeholders **monitor sales performance, identify high-performing markets and products, understand customer purchasing behavior, and uncover areas requiring further investigation or strategic action**.

---



## 👤 Author

### **Anurag Kumar Poddar**

**Data Analyst | Power BI | SQL | Python | Excel | Data Visualization**

<p>
  <a href="https://github.com/anuragkumarpoddar-ui">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white"/>
  </a>
  <a href="https://www.linkedin.com/in/anurag-kumar-poddar-51239596/">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
  </a>
</p>

---

⭐ **If you find this project useful or interesting, consider giving the repository a star!**
