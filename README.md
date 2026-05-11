# E-commerce Sales and Profit Analysis

# Table of Content
•	[Project Overview](#project-overview)

•	[Dataset Description](#dataset-description)

•	[Data Sources](#data-sources)

•	[Structure](#structure)

•	[Tools](#tools)

•	[Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)

•	[Sales Analysis and Profit Analysis](#sales-analysis-and-profit-analysis)

•	[Dashboard Report](#dashboard-report)

•	[Key Findings and Insights](#key-findings-and-insights)

•	[Recommendations](#recommendations)

# Project Overview

This data analysis aims to provide insights into the sales performance transactions across different products, categories, and regions, along with quantity, revenue, and profit details.

# Dataset Description
The dataset consists of 3,500 e-commerce orders with 7 key features. It captures sales transactions across different products, categories, and regions, along with quantity, revenue, and profit details.

The data is complete, contains no missing values, and reflects realistic business patterns suitable for analytical and predictive tasks.

# Data Sources
[Download for Free Here at Kaggle.com](https://www.kaggle.com/datasets/nalisha/e-commerce-sales-and-profit-analysis-dataset/data)

# Structure 
|| Column | Description | Non_null_count | Data-type |
|-|--------|-------------|----------------|-----------|
|1| Order Date|	Date of ordering [Day/Monthly/Year]	|3500	|object|
|2|Product Name	|Product ordered ['Printer', 'Mouse', 'Tablet', 'Camera', 'Headphones', 'Smartwatch', 'Monitor', 'Smartphone', 'Keyboard', 'Laptop']|	3500|	object|
|3|Category|	Product category ['Office', 'Accessories', 'Electronics']|	3500|	object|
|4|Region	|Geographic location ['North', 'East', 'South', 'West']|	3500|	object|
|5|Quantity	|Number of products ordered	|3500	|int64|
|6|Sales	|Min: 51, Max: 10,782	|3500	|int64|
|7|Profit|	Min: 6.97, Max: 2,946.93|	3500|	float64|

# Tools
- Excel – Data Cleaning
- Python, DAX – Data Analysis
- Power BI – Creating report [Download for Free Here]( https://www.microsoft.com/en-us/power-platform/products/power-bi/downloads?ocid=ORSEARCH_Bing&msockid=2c328bbf2b3167101ab79c8d2ab46616)

# Exploratory Data Analysis (EDA)
ED = "ecommerce-sales-data.csv"

## Descriptive Statistics
```Python
ED.describe(include='all')
```
 <img width="837" height="415" alt="36" src="https://github.com/user-attachments/assets/20240818-4e9e-4222-b981-374079dc15b9" />

## Missing Values Checks
```python
ED.isnull().sum()
ED.notnull().sum()
```
|Missing Data|Non-null Data|
|------------|-------------|
|<img width="380" height="350" alt="Missing data" src="https://github.com/user-attachments/assets/9c58bd41-5105-4325-a7d1-7365bc6548c2" />| <img width="380" height="350" alt="Non-null" src="https://github.com/user-attachments/assets/cdc049db-97de-40f3-b982-f967b5ff678e" />|

The analysis indicates that the dataset contains no missing values.

### Product Categories
```python
ED['Category'].value_counts()\
ED['Category'].value_counts().plot(kind='pie')
plt.show()
```
|ED['Category'].value_counts()|ED['Category'].value_counts().plot(kind='pie') plt.show()|
|--|--|
|<img width="400" height="360" alt="Screenshot 2026-05-11 004755" src="https://github.com/user-attachments/assets/576c3a00-6c6b-48cd-b282-e716379d702f" />|<img width="458" height="438" alt="Category 1" src="https://github.com/user-attachments/assets/a0a8bfda-ec2d-418e-811a-503f03309330" />|


# Sales Analysis and Profit Analysis
- Sale by Product name
- Sale by Product category
- Profit by Product name
- Profit by Product category 

# Dashboard Report
### Dasboard:
<img width="857" height="457" alt="Screenshot 2026-05-09 174927" src="https://github.com/user-attachments/assets/d2193eb0-44f0-4180-ae99-507d9e32bc1c" /> 

### Detailed Summary Tables:

```DAX
Total Quantites = SUM('ecommerce_sales_data (2)'[Quantity])
Total Profit = SUM('ecommerce_sales_data (2)'[Profit])
Total Sales = SUM('ecommerce_sales_data (2)'[Sales])
```
<img width="857" height="457" alt="Screenshot 2026-05-09 175007" src="https://github.com/user-attachments/assets/d1e22cc8-d7e4-4a9e-9112-a44e10c7d850" />

# Key Findings and Insights
- Cameras recorded the highest product sales overall, with the South region contributing the largest share of camera sales distribution.
- The West region achieved the highest overall sales performance, recording 2,844,450 units sold.
- Yearly analysis showed that 2023 recorded the highest overall sales and profit. Possible contributing factors may include inflation, shifts in consumer behavior, increased disposable income, or broader market dynamics.
- Out of the total sales volume of 10.67 million units across the Electronics, Accessories, and Office categories, Electronics accounted for 49.93% of total sales, making it the leading product category.
  
# Recommendations
- Further investigation is recommended to determine the key factors driving this performance, as the available dataset provides limited variables for comprehensive causal analysis.
- The Electronics category demonstrates strong revenue-generation and profit potential, indicating that it should be prioritized within the company’s sales and growth strategy.

