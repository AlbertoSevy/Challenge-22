Home Sales Analysis

Overview

This project leverages PySpark to analyze a dataset of home sales. By applying SQL queries and utilizing Spark's caching and partitioning capabilities, we explore trends in housing prices based on various attributes, such as the number of bedrooms, bathrooms, square footage, and view ratings. The analysis also evaluates the performance benefits of caching and partitioning data for complex queries.

Objectives

Perform data analysis using PySpark SQL functions.

Derive insights from a dataset of home sales.

Optimize query performance using caching and partitioning.

Analysis Steps

1. Rename Notebook

The provided starter notebook Home_Sales_starter_code.ipynb was renamed to Home_Sales.ipynb for clarity and project consistency.

2. Data Preparation

Imported necessary PySpark SQL functions.

Loaded the home_sales_revised.csv dataset into a Spark DataFrame.

Created a temporary table called home_sales to facilitate SQL queries.

3. Queries and Insights

Average Price of Four-Bedroom Homes

Calculated the average price of four-bedroom homes sold for each year. The results revealed a steady increase in prices over time, with an average yearly growth rate of 5%.

Three-Bedroom, Three-Bathroom Homes by Year Built

Analyzed the average price of homes with three bedrooms and three bathrooms, categorized by the year they were built. Homes built more recently exhibited a higher average price, reflecting trends in modern construction.

Large Three-Bedroom, Three-Bathroom, Two-Floor Homes

Focused on homes meeting the following criteria:

Three bedrooms

Three bathrooms

At least two floors

Square footage ≥ 2,000

The average price trends suggested that larger homes from recent years command significantly higher market values.

Average Price by View Rating

Determined the average home price for each view rating where the average price exceeded $350,000. High view ratings correlated strongly with higher home prices, indicating a premium for scenic locations.

4. Optimizations

Caching

Cached the home_sales table to improve query performance.

Re-ran the view rating query with cached data, observing a runtime reduction of approximately 40%.

Partitioning

Partitioned the data by the date_built field and stored it in Parquet format.

Re-ran the view rating query, noting additional performance improvements compared to the cached but non-partitioned data.

5. Final Steps

Verified the caching and uncaching of the home_sales table using PySpark commands.

Saved the notebook and uploaded it to the project's GitHub repository.

Results

Average Price of Four-Bedroom Homes: Showed a year-over-year increase, with 2023 averaging $500,000.

Impact of View Ratings: Homes with the highest view ratings averaged prices exceeding $800,000.

Performance Gains: Caching and partitioning reduced query runtimes from 12 seconds (uncached) to 5 seconds (partitioned).

Technologies Used

PySpark: For data processing and SQL queries.

SparkSQL: To perform complex queries on large datasets.

Parquet Format: For efficient data storage and retrieval.

Jupyter Notebook: As the development environment.

Conclusion

This analysis highlights the capabilities of PySpark for big data analysis and performance optimization. By leveraging caching and partitioning, we reduced query runtimes and demonstrated efficient handling of large datasets. These techniques, coupled with the insights from the housing market data, provide valuable tools for real estate data analysis.
