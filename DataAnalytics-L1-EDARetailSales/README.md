# Retail Sales Data Analysis

## Project Overview
This project performs Exploratory Data Analysis (EDA) on retail customer purchase data as part of the Oasis Infobyte Data Analytics Internship – Task 1.

The goal is to understand customer purchasing patterns, product category performance, and purchase trends using Python.

## Objectives
- Load and inspect the retail dataset.
- Check missing values and duplicate records.
- Calculate mean, median, mode, and standard deviation.
- Analyze monthly and quarterly purchase trends.
- Explore customer age groups and gender distribution.
- Identify the top 10 products by total purchase amount.
- Compare purchase amounts across product categories.
- Analyze correlations between numerical variables.
- Study repeat customer and discount patterns.
- Provide actionable business recommendations.

## Dataset
**Dataset file:** `Walmart_customer_purchases.csv`

The dataset contains 50,000 customer purchase records and 12 columns, including:
- Customer ID
- Age
- Gender
- City
- Product category
- Product name
- Purchase date
- Purchase amount
- Payment method
- Discount applied
- Rating
- Repeat customer status

## Tools and Technologies
- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn

## Project Workflow
1. Loaded and inspected the dataset.
2. Checked missing values and duplicate records.
3. Converted purchase dates and created month, quarter, and age-group columns.
4. Calculated descriptive statistics.
5. Analyzed monthly and quarterly purchase trends.
6. Visualized customer demographics.
7. Identified the top 10 products by total purchase amount.
8. Compared purchase amounts across product categories.
9. Created a correlation heatmap.
10. Analyzed repeat customers and discount patterns.
11. Developed business recommendations based on the analysis.

## Visualizations

### 1. Monthly Trend
This chart shows how total purchase amounts change from month to month.

![Monthly Trend](screenshots/Monthly%20trend.png)

### 2. Category Analysis
This chart compares total purchase amounts across product categories.

![Category Analysis](screenshots/Category%20analysis.png)

### 3. Correlation Heatmap
This chart shows the relationships between numerical variables such as age, purchase amount, and rating.

![Correlation Heatmap](screenshots/Correlation%20heatmap.png)

## Business Recommendations
- **Inventory planning:** Monitor high-performing products and categories to support stock planning.
- **Sales improvement:** Investigate months with lower purchase amounts and test suitable promotional campaigns.
- **Customer retention:** Use repeat-customer purchasing patterns to develop relevant loyalty strategies.
- **Discount evaluation:** Compare purchase patterns across discount groups before expanding discount campaigns.
- **Better business analysis:** Collect product cost, profit, and quantity data to support profitability and unit-sales analysis.

## Limitations
- The analysis focuses on purchase amounts and customer purchasing patterns.
- Product cost and profit data are not available, so profitability cannot be calculated directly.
- The top 10 products are ranked by total purchase amount, not by units sold.
- Findings and recommendations are based on the available dataset.

## Conclusion
This project uses Python-based exploratory data analysis and visualizations to understand retail customer behavior, purchase trends, and product category performance. The results can help support inventory planning, sales improvement, and customer retention decisions.

## Project Structure
```text
DataAnalytics-L1-EDARetailSales/
├── data/
│   └── Walmart_customer_purchases.csv
├── screenshots/
│   ├── Monthly trend.png
│   ├── Category analysis.png
│   └── Correlation heatmap.png
├── EDA_Retail_Sales.ipynb
└── README.md
```

## Author
Data Analytics Internship Candidate

**Internship:** Oasis Infobyte  
**Track:** Data Analytics  
**Task:** Task 1 – EDA on Retail Sales Data