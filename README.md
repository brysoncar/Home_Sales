# Home_Sales

This repository contains code for analyzing home sales data using PySpark in a Google Colab environment. The analysis includes various queries performed on the dataset, such as calculating average prices, filtering based on specific criteria, and determining runtime for queries. In order to complete this analysis I rellied heavily on the AI assistant in colab, I also choose to use Pandas style commands to SQL style commands as was learned in class as Pandas is prefered by my current coworkers. 

Installation
To run this code, you need to have PySpark installed. You can install it using pip:

bash
Copy code
pip install pyspark
Additionally, you need to install the findspark package to locate the Spark installation:

bash
Copy code
pip install findspark
Usage
The notebook home_sales_analysis.ipynb provides step-by-step instructions and code for performing various analyses on the home sales dataset. You can run the notebook in a Google Colab environment or any other environment that supports PySpark.

Contents
home_sales_analysis.ipynb: Jupyter notebook containing the code for analyzing home sales data.
partitioned_home_sales_data/: Directory containing partitioned parquet data.
README.md: This README file.
Steps
Reading Data: Read the home sales data from an AWS S3 bucket into a DataFrame.
Creating Temporary View: Create a temporary view of the DataFrame for easy querying.
Average Price for Four Bedroom Houses: Calculate the average price for four-bedroom houses sold in each year.
Average Price for 3 Bed, 3 Bath Homes: Calculate the average price of homes with 3 bedrooms and 3 bathrooms for each year built.
Average Price for Specific Criteria: Calculate the average price of homes meeting specific criteria (3 bedrooms, 3 bathrooms, 2 floors, and >= 2,000 sqft) for each year built.
View Rating for Expensive Homes: Find the "view" rating for the average price of homes with prices greater than or equal to $350,000.
Caching Data: Cache the temporary table home_sales for faster access.
Checking Cache: Verify if the table is cached.
Querying Cached Data: Run a query using the cached data and compare runtime with the uncached version.
Partitioning Data: Partition the home sales data by the date_built field and save it in parquet format.
Reading Partitioned Data: Read the partitioned parquet data.
Creating Temporary Table for Parquet Data: Create a temporary table for the partitioned parquet data.
Querying Parquet Data: Run a query on the partitioned parquet data and compare runtime with previous queries.
Uncaching Data: Uncache the temporary table home_sales.
Checking Cache Status: Verify if the table is no longer cached.
Contributors
[Your Name]
Feel free to modify and extend this code for your own analysis. If you encounter any issues or have suggestions for improvements, please create an issue in the repository.
