# Sales Data Analysis Project

## Project Overview
This project focuses on analyzing sales data to discover insights that help businesses make better decisions. The analysis was performed using Python and data visualization techniques.

## Objectives
- Understand sales trends
- Identify top-performing products
- Analyze customer purchasing behavior
- Generate insights using data visualization

## Tools & Technologies
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## Dataset
The dataset contains sales information including:
- Order ID
- Product Name
- Sales
- Quantity
- Category
- Date of Purchase

## Data Analysis Steps
1. Data Collection
2. Data Cleaning
3. Data Exploration
4. Data Visualization
5. Insight Generation

## Key Insights
- Identified the top-selling products
- Found seasonal trends in sales
- Analyzed revenue contribution by category
- Discovered customer purchase patterns

## Visualizations
The project includes several visualizations such as:
- Sales Trend Graph
- Category-wise Sales
- Product Performance Charts

## How to Run the Project

1. Clone the repository
2. 
3. Install required libraries

pip install pandas numpy matplotlib seaborn

3. Run the Jupyter Notebook

jupyter notebook

## Future Improvements
- Build an interactive dashboard
- Apply machine learning for sales prediction
- Automate data pipeline

## Author
Your Name


## Sales Insights Data Analysis Project

1. SQL database dump is in db_dump.sql file above. Download `db_dump.sql` file to your local computer and import it as per instructions given in the tutorial video

### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`


Data Analysis Using Power BI
============================

1. Formula to create norm_amount column

`= Table.AddColumn(#"Filtered Rows", "norm_amount", each if [currency] = "USD" or [currency] ="USD#(cr)" then [sales_amount]*75 else [sales_amount], type any)`



