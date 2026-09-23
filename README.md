# Data_Projects
# NYC Bus Delays ETL Pipeline

An end-to-end data engineering project that processes NYC Bus Breakdown and Delays open data using Polars, converts the cleaned dataset to Parquet, loads it into Google BigQuery, and performs SQL-based analysis.

## Pipeline

CSV → Polars → Parquet → Google BigQuery → SQL Analytics

## Dataset

NYC Bus Breakdown and Delays open dataset.

- Rows processed: 1,297,681
- Final columns: 31

## Technologies

- Python
- Polars
- Parquet
- Google Colab
- Google BigQuery
- SQL

## Key Transformations

- Schema inspection and datatype conversion
- Timestamp parsing
- Null-value analysis
- Student-count cleaning
- Delay-duration standardization
- Creation of minimum, maximum, and average delay metrics
- Date feature engineering
- Data-quality validation
- Parquet conversion with Snappy compression

## Data Quality

The pipeline preserves questionable source records and flags them instead of deleting them.

- VALID: 1,268,884
- SAME_DAY_ORDER_ISSUE: 28,731
- DATE_SEQUENCE_ISSUE: 65
- MISSING_DATE: 1

## Key Findings

- Heavy Traffic was the most common incident reason.
- Brooklyn had the highest number of recorded incidents.
- 7 AM had the highest incident volume.
- Late return from Field Trip had the highest average parsed delay among major delay categories.

## Notebook

See `NYC_Bus_Delays_ETL_Pipeline.ipynb` for the complete ETL workflow and BigQuery analysis.
