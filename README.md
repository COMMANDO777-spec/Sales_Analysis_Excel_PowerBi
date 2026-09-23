# Sales Analysis Excel PowerBi

## Project Overview

Retail Sales Analysis is a data analytics project designed to simulate a real-world retail sales reporting workflow.

The project starts with raw retail transaction data containing data-quality issues. The data was cleaned and transformed using **Microsoft Excel**, followed by the development of an interactive **Power BI dashboard** to analyze sales, customers, products, cities, and payment methods.

## Tools & Technologies

* Microsoft Excel
* Power BI
* DAX
* Data Cleaning
* Data Transformation
* Data Visualization
* Business Intelligence

## Project Workflow

```text
Raw Sales Data
      ↓
Data Cleaning & Validation in Excel
      ↓
Calculated Columns
      ↓
Data Quality Checks
      ↓
Power BI
      ↓
DAX Measures
      ↓
Interactive Dashboard
      ↓
Business Insights
```

---

## Data Cleaning

The raw dataset contained several realistic data-quality problems, including:

* Duplicate transactions
* Missing customer information
* Missing discount values
* Inconsistent capitalization
* Extra spaces
* Inconsistent product categories
* Invalid quantities
* Invalid customer ratings
* Missing age values

The data was cleaned and standardized before being imported into Power BI.

### Cleaning techniques used

* Remove Duplicates
* `TRIM()`
* `PROPER()`
* `IF()`
* `AVERAGE()`
* `MEDIAN()`
* `MONTH()`
* `YEAR()`
* Data validation
* Filtering and sorting

---

## Data Transformation

Additional analytical columns were created in Excel:

* Gross Sales
* Discount Amount
* Net Sales
* Month
* Month Number
* Year
* Customer Segment

### Sales calculation

```text
Gross Sales = Quantity × Unit Price

Discount Amount = Gross Sales × Discount

Net Sales = Gross Sales − Discount Amount
```

---

# Power BI Dashboard

The dashboard provides an overview of NovaMart's retail sales performance.

### Key Performance Indicators

The dashboard currently displays:

* **Total Sales:** ₹388K
* **Total Orders:** 48
* **Units Sold:** 82
* **Total Customers:** 48
* **Average Order Value:** ₹8.09K

---

## Dashboard Analysis

### Sales by Category

The dashboard compares total sales across product categories, including:

* Electronics
* Furniture
* Accessories
* Footwear
* Electronic

The visualization also helped identify a **category-standardization issue** where `Electronics` and `Electronic` appear separately. This is an example of a data-quality issue that can affect business reporting.

---

### Sales by City

Sales are analyzed across different cities.

The dashboard shows cities including:

* Pune
* Mumbai
* Noida
* Ahmedabad
* Bangalore
* Delhi
* Kolkata
* Hyderabad
* Chennai
* Lucknow
* Chandigarh
* Jaipur
* Kochi
* Unknown

This allows sales performance to be compared geographically.

---

### Sales Trend

A time-series visualization is used to analyze sales across:

* Year
* Quarter
* Month
* Day

This helps identify changes and spikes in sales over time.

---

### Payment Method Analysis

The dashboard analyzes order distribution across:

* UPI
* Card
* Cash

The current dashboard shows:

| Payment Method | Orders |  Share |
| -------------- | -----: | -----: |
| UPI            |     22 | 45.83% |
| Card           |     19 | 39.58% |
| Cash           |      7 | 14.58% |

---

## DAX Measures

The Power BI dashboard uses DAX measures such as:

```DAX
Total Sales =
SUM(Cleaned_Sales[Net Sales])
```

```DAX
Total Orders =
DISTINCTCOUNT(Cleaned_Sales[Order_ID])
```

```DAX
Units Sold =
SUM(Cleaned_Sales[Quantity])
```

```DAX
Average Order Value =
DIVIDE([Total Sales], [Total Orders])
```

```DAX
Total Customers =
DISTINCTCOUNT(Cleaned_Sales[Customer_ID])
```

---

## Business Questions

The dashboard was designed to answer questions such as:

1. What are the total sales?
2. How many orders were placed?
3. What is the average order value?
4. Which product category generates the most sales?
5. Which cities generate the most sales?
6. How do sales change over time?
7. Which payment method is most commonly used?
8. Which products and categories perform best?
9. Which customer segments contribute most to sales?
10. Which stores and salespeople perform best?

---

## Key Skills Demonstrated

This project demonstrates practical experience with:

* Excel data cleaning
* Data quality analysis
* Data transformation
* Data validation
* Excel formulas
* Business metrics
* Power BI
* DAX
* Data visualization
* Dashboard development
* Business-oriented analysis

---


## Project Objective

The objective of this project was to simulate an end-to-end **junior data analyst workflow**:

> **Clean raw data → validate data quality → transform data → analyze KPIs → build an interactive dashboard → communicate business information through visualizations.**
