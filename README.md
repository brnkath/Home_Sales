# Using Google Colab and SparkSQL to determine key metrics about home sales data

## Contributor: Brian Kath

## Repository Structure

- Main Folder
  - .gitignore
  - Home_Sales.ipynb
  - README.md

## Overview

For this project, I used Google Colab and SparkSQL to determine key metrics about home sales data. To set up the project, I imported all necessary PySpark SQL functions that were needed, and I read in a CSV file containing data on home sales.

Next, I created a temporary view so I could answer several questions using the data. The specific questions answered were:

- What is the average price for a four-bedroom house sold for each year? Rounding off each answer to two decimal places.
- What is the average price of a home for each year it was built that has three bedrooms and three bathrooms? Rounding off each answer to two decimal places.
- What is the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Rounding off each answer to two decimal places.
- What is the "view" rating for homes costing more than or equal to $350,000? Also, determining the run time for this query, and rounding off each answer to two decimal places.

Then, I cached the temporary table and used the cached data to run the query for the fourth question again. I also calculated the run time for this query using the cached data, so it could be compared to the original query. I then partitioned the data for the date_built field on formatted parquet home sales data and created a temporary table for parquet data. I then ran the same query regarding the fourth question in this project and calculated the run time for the query, so it could be compared to the other two similar queries.
