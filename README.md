# Flight Data Analysis

## Overview
This project analyzes flight data using **PySpark** to uncover insights about flight delays, trends, and correlations. The analysis includes **data preprocessing, exploratory data analysis (EDA), and visualization** to highlight key patterns.

## Dataset Details
- **File Name:** `flight_data-1.csv`
- **Format:** CSV
- **Columns Include:** `YEAR`, `MONTH`, `DAY`, `Flight_Number`, `Flight_Date`, `Airline`, `Departure_Delay`, `Arrival_Delay`, `Distance`, etc.
- **Total Rows & Columns:** Run the provided PySpark script to determine exact counts.

## Analysis Approach
1. **Data Loading:** Read the dataset into a PySpark DataFrame.
2. **Data Preprocessing:**
   - Convert `YEAR`, `MONTH`, `DAY` into a `Flight_Date` column.
   - Handle missing values and type conversions.
3. **Exploratory Data Analysis (EDA):**
   - Generate summary statistics.
   - Visualize trends, delays, and correlations.
4. **Comparison of PySpark DataFrames & RDDs:**
   - Discuss advantages and disadvantages of both.

## Visualizations Included
- **Flight Delay Distribution**
- **Average Delay by Airline**
- **Monthly Flight Trends**
- **Correlation Heatmap**

## How to Run the Analysis
1. Ensure you have **PySpark** installed:
   ```bash
   pip install pyspark
   ```
2. Run the script in a PySpark-supported environment:
   ```python
   from pyspark.sql import SparkSession
   spark = SparkSession.builder.appName("FlightDataAnalysis").getOrCreate()
   df = spark.read.csv("flight_data-1.csv", header=True, inferSchema=True)
   print(f"Rows: {df.count()}, Columns: {len(df.columns)}")
   ```
3. Use Jupyter Notebook or a Python script to execute the analysis.

## Future Enhancements
- Implement machine learning models for **delay prediction**.
- Explore **real-time flight data streaming** using PySpark.

## Author
- **Vivek Menon**

For any questions, feel free to reach out!

