# Sales-Analysis-Tableau

## Sales Insight Analysis Project

This project focuses on analyzing sales data to gain valuable insights using Tableau and MySQL. The aim is to provide a comprehensive understanding of the sales performance and identify key trends and patterns that can inform decision-making and improve business strategies.

## Table of Contents
## Project Overview
## Technologies Used
## Data Sources
## Data Analysis
## SQL Query
## How to Use
## Contributing
## License

## Project Overview

The Sales Insight Analysis project leverages Tableau and MySQL to explore and visualize sales data, enabling data-driven decision-making for better business outcomes. By analyzing sales performance, trends, and patterns, this project aims to provide actionable insights that can optimize sales strategies, identify growth opportunities, and improve overall performance.

## Technologies Used

Tableau: A powerful data visualization tool that allows for interactive exploration and analysis of data.
MySQL: A popular open-source relational database management system used for storing and managing large datasets.
Data Sources
The project utilizes a MySQL database as the primary data source for sales information. The database contains tables with relevant data fields such as sales date, product details, customer information, revenue, and other relevant metrics.

## Data Analysis

The data analysis process involves the following steps:

Data Extraction: Extracting the required sales data from the MySQL database.
Data Cleaning: Cleaning the data to ensure accuracy, consistency, and completeness.
Data Transformation: Transforming the data into a format suitable for analysis, such as aggregating sales by various dimensions (e.g., product, region, time).
Data Visualization: Creating interactive and insightful visualizations using Tableau to explore patterns, trends, and relationships within the data.
Insight Generation: Deriving meaningful insights and conclusions from the data visualizations, identifying key performance indicators (KPIs), and highlighting areas of improvement.

## SQL Query

- Show all customer records

SELECT * FROM customers;

- Show total number of customers

SELECT count(*) FROM customers;

- Show transactions for Chennai market (market code for chennai is Mark001

SELECT * FROM transactions where market_code='Mark001';

- Show distinct product codes that were sold in chennai

SELECT distinct product_code FROM transactions where market_code='Mark001';

- Show transactions where currency is US dollars

SELECT * from transactions where currency="USD"

- Show transactions in 2020 join by date table

SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;

- Show total revenue in year 2020,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";

- Show total revenue in year 2020, January Month,

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");

- Show total revenue in year 2020 in Chennai

SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";


## How to Use

To utilize this project for sales insight analysis:

1. Set up a MySQL database and import the relevant sales data.
2. Install Tableau and open the Tableau workbook.
3. Customize the data extraction, cleaning, and visualization steps based on your specific requirements.
4. Explore the Tableau visualizations to gain insights and make informed decisions.

## Contributing

Contributions to this project are welcome. If you have any suggestions, improvements, or bug fixes, please submit a pull request.

## License

This project is licensed under the MIT License. Feel free to use and modify the code as per the license terms.





