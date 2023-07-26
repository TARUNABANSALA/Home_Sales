Big Data Challenge
This challenge involved using knowledge of SparkSQL to determine key metrics about home sales data. Spark was then used to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table had been uncached.

Instructions
Rename the Home_Sales_starter_code.ipynb file as Home_Sales.ipynb.

Import the necessary PySpark SQL functions for this assignment.

Read the home_sales_revised.csv data in the starter code into a Spark DataFrame.

Create a temporary table called home_sales.

Answer the following questions using SparkSQL:
What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.

Screenshot 2023-07-24 at 10 04 49 PM
What is the average price of a home for each year it was built that has three bedrooms and three bathrooms? Round off your answer to two decimal places.

Screenshot 2023-07-24 at 10 05 38 PM
What is the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.

Screenshot 2023-07-24 at 10 07 32 PM
What is the "view" rating for homes costing more than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.

Screenshot 2023-07-24 at 10 08 06 PM
Cache your temporary table home_sales.

Check if your temporary table is cached.

Using the cached data, run the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.

Partition by the "date_built" field on the formatted parquet home sales data.

Create a temporary table for the parquet data.

Run the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.

Uncache the home_sales temporary table.

Verify that the home_sales temporary table is uncached using PySpark.

Download your Home_Sales.ipynb file and upload it into your "Home_Sales" GitHub repository.