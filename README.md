Big Data Challenge
This challenge involved using knowledge of SparkSQL to determine key metrics about home sales data. Spark was then used to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table had been uncached.

Instructions
I have renamed renamed the Home_Sales_starter_code_colab.ipynb file as Home_Sales_google_colab.ipynb.

Import the necessary PySpark SQL functions for this assignment.

Read the home_sales_revised.csv data in the starter code into a Spark DataFrame.

Create a temporary table called home_sales.

Answer the following questions using SparkSQL:
What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.
+----+---------+
|year|avg_price|
+----+---------+
|2022|296363.88|
|2021|301819.44|
|2020|298353.78|
|2019| 300263.7|

What is the average price of a home for each year it was built that has three bedrooms and three bathrooms? Round off your answer to two decimal places.
+----+---------+
|year|avg_price|
+----+---------+
|2022|292725.69|
|2021|294211.46|
|2020|294204.16|
|2019|287287.82|
+----+---------+

What is the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.
+----+---------+
|year|avg_price|
+----+---------+
|2022|289517.82|
|2021|296330.96|
|2020|292289.09|
|2019|289976.57|
+----+---------+


What is the "view" rating for homes costing more than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.
+----+----------+
|view| avg_price|
+----+----------+
| 100| 1026669.5|
|  99|1061201.42|
|  98|1053739.33|
|  97|1129040.15|
|  96|1017815.92|
|  95| 1054325.6|
|  94| 1033536.2|
|  93|1026006.06|
|  92| 970402.55|
|  91|1137372.73|
+----+----------+


Cache your temporary table home_sales.
DataFrame[] 

Check if your temporary table is cached.
True

Using the cached data, run the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
+----+----------+
|view| avg_price|
+----+----------+
| 100| 1026669.5|
|  99|1061201.42|
|  98|1053739.33|
|  97|1129040.15|
|  96|1017815.92|
|  95| 1054325.6|
|  94| 1033536.2|
|  93|1026006.06|
|  92| 970402.55|
|  91|1137372.73|
+----+----------+
only showing top 10 rows

--- 0.421419620513916 seconds ---
--- 0.4214956760406494 seconds ---

Partition by the "date_built" field on the formatted parquet home sales data.
+--------------------+----------+------+--------+---------+-----------+--------+------+----------+----+----------+
|                  id|      date| price|bedrooms|bathrooms|sqft_living|sqft_lot|floors|waterfront|view|date_built|
+--------------------+----------+------+--------+---------+-----------+--------+------+----------+----+----------+
|2ed8d509-7372-46d...|2021-08-06|258710|       3|        3|       1918|    9666|     1|         0|  25|      2015|
|941bad30-eb49-4a7...|2020-05-09|229896|       3|        3|       2197|    8641|     1|         0|   3|      2015|
|c797ca12-52cd-4b1...|2019-06-08|288650|       2|        3|       2100|   10419|     2|         0|   7|      2015|
|0cfe57f3-28c2-472...|2019-10-04|308313|       3|        3|       1960|    9453|     2|         0|   2|      2015|
|d715f295-2fbf-4e9...|2021-05-17|391574|       3|        2|       1635|    8040|     2|         0|  10|      2015|
+--------------------+----------+------+--------+---------+-----------+--------+------+----------+----+----------+
only showing top 5 rows

Create a temporary table for the parquet data.

Run the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
+----+----------+
|view| avg_price|
+----+----------+
| 100| 1026669.5|
|  99|1061201.42|
|  98|1053739.33|
|  97|1129040.15|
|  96|1017815.92|
+----+----------+
only showing top 5 rows

--- 0.5114290714263916 seconds ---

Uncache the home_sales temporary table.

Verify that the home_sales temporary table is uncached using PySpark.
