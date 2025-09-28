# Chinook Database Sales Analysis
## Overview
This project analyzes product sales data from the Chinook SQLite database using SQL queries executed through Python. The goal is to extract key business insights such as:

- Top-selling tracks by quantity sold  
- Revenue generated per region  
- Monthly sales performance trends  
- Ranking of top tracks by revenue using SQL window functions  
Results are saved as CSV files for further analysis or reporting.

## Dataset
- **Source:** [Chinook Database (Kaggle)](https://www.kaggle.com/datasets/lerocha/chinook-database)
- The Chinook database is a sample database representing a digital media store, containing tables such as Invoice, InvoiceLine, Track, Customer, and more.

## Technologies Used
- **SQLite**: For running SQL queries on the Chinook database file  
- **Python (pandas, sqlite3)**: To connect to the database, run queries, and export results  
- **SQL window functions**: Used for ranking and advanced aggregation  

## How to Run

1. Place the `Chinook_Sqlite.sqlite` database file in your working directory or update the connection path in the script accordingly.

2. Run the Python script `chinook_analysis.py` (or your script file name) that contains the SQL queries and export logic.

3. The script will generate the following CSV output files in the same directory:
   - `top_10_tracks_by_quantity.csv`  
   - `revenue_per_region.csv`  
   - `monthly_sales_performance.csv`  
   - `top_10_tracks_ranked_by_revenue.csv`

4. Each CSV file contains query results ready for further analysis or visualization.

## Description of Queries

### 1. Top-Selling Tracks by Quantity
- Aggregates total quantity sold per track.
- Lists top 10 tracks with the highest sales quantity.

### 2. Revenue Per Region
- Calculates total revenue generated from invoices grouped by billing country.
- Sorts countries by descending revenue.

### 3. Monthly Sales Performance
- Aggregates total revenue and number of invoices by month.
- Helps identify trends and seasonality.

### 4. Top Tracks Ranked by Revenue
- Calculates total revenue per track.
- Uses SQL `RANK()` window function to rank top 10 tracks by revenue.

