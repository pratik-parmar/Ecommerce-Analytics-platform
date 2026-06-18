PySpark E-Commerce Sales Analytics Platform
Overview

This project is an end-to-end Data Engineering and Analytics solution built using PySpark and the Brazilian Olist E-Commerce Dataset.

The project follows the Medallion Architecture (Bronze, Silver, Gold) to ingest, clean, transform, and analyze e-commerce data. It generates business insights related to sales performance, customer behavior, product performance, customer retention, and revenue forecasting.

The goal of this project is to demonstrate real-world Data Engineering concepts including ETL pipelines, data warehousing, analytics, data quality validation, and machine learning-based forecasting.

Project Objectives
Build scalable ETL pipelines using PySpark
Implement Bronze, Silver, and Gold data layers
Create analytical datasets for reporting
Analyze customer purchasing behavior
Identify top-performing products
Track sales trends over time
Measure customer retention
Forecast future sales revenue
Implement production-style data quality checks
Dataset

Dataset: Olist Brazilian E-Commerce Dataset

The dataset contains information about:

Customers
Orders
Products
Sellers
Payments
Reviews
Order Items

Source: Kaggle

Tech Stack
Data Engineering
Python
PySpark
Spark SQL
Parquet
Data Processing
Pandas
Machine Learning
Scikit-Learn
Linear Regression


Project Architecture

Raw Data
↓
Bronze Layer
↓
Silver Layer
↓
Gold Layer
↓
Analytics Layer
↓
Forecasting Layer

Bronze Layer

Raw data ingestion from source files.

Examples:

Customers
Orders
Products
Payments
Reviews

Stored as Parquet files.

Silver Layer

Data cleaning and transformation.

Tasks:

Remove duplicates
Handle null values
Standardize formats
Extract date attributes
Gold Layer

Business-ready analytical datasets.

Example:

Sales Fact Table

Contains:

Order Details
Customer Information
Product Information
Revenue Metrics
Time Dimensions
Project Structure

ecommerce-pyspark-project/

data/

output/
├── bronze/
├── silver/
├── gold/
├── analytics/
└── dashboard/

src/
├── 01_create_spark_session.py
├── 02_ingest_raw_data.py
├── 03_clean_customers.py
├── 04_clean_orders.py
├── 05_create_sales_fact.py
├── 06_customer_analytics.py
├── 07_product_analytics.py
├── 08_sales_trend_analysis.py
├── 09_customer_retention.py
├── 10_sales_forecasting.py
├── 11_sales_dashboard_dataset.py
└── 12_data_quality_checks.py



ETL Pipeline
1. Data Ingestion
Download dataset
Load CSV files into Spark DataFrames
Store raw data in Bronze Layer

3. Data Cleaning
Remove duplicates
Handle missing values
Validate records

4. Data Transformation
Create date dimensions
Extract year, month, quarter, weekday
Build analytical datasets

5. Data Modeling
Create Sales Fact Table
Join Orders, Products, Payments, and Customers

6. Analytics

Generate insights such as:

Top Customers
Product Performance
Revenue Trends
Customer Retention
Customer Lifetime Value

7. Forecasting

Predict future monthly revenue using machine learning.

1. Analytics Implemented

Customer Analytics
Top customers by revenue
Average order value

2. Total orders per customer

3. Product Analytics
Top-selling products
Revenue by category
Product popularity analysis

4. Sales Trend Analysis

Monthly revenue trends
Year-over-year performance
Seasonal patterns

5. Customer Retention

Repeat customers
Retention rate
Customer lifetime value (CLV)

6. Sales Forecasting

Monthly revenue prediction
Future sales projections
