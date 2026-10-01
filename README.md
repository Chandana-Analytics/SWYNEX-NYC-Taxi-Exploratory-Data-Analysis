# SWYNEX - NYC Taxi Exploratory Data Analysis

## Project Overview

This project is part of my SWYNEX Technologies Data Analytics Internship - Task 2.

In this task, I performed exploratory data analysis on the cleaned NYC Yellow Taxi dataset prepared during Task 1.

The analysis was done to understand trip patterns, taxi demand at different times, payment distribution, high-activity locations and unusual records in the dataset.

## Dataset

- Dataset: NYC Yellow Taxi Trip Records
- Period: January 2026
- Original records: 3,724,889
- Cleaned records: 3,724,777
- Records removed during cleaning: 112
- Columns: 20
- Source: NYC Taxi & Limousine Commission (TLC)

The dataset was cleaned during Task 1 before starting this analysis.

Source: https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

## Tools Used

- Snowflake
- SQL
- Excel
- GitHub

Snowflake was used for the analysis and calculations.

SQL was used to calculate statistics, distributions, time-based demand, payment patterns, location activity and anomalies.

Excel was used to create the charts.

GitHub was used to organize and submit the project files.

## Analysis Performed

### 1. Overall Statistics

Calculated statistics for:

- Total number of trips
- Trip distance
- Trip duration
- Fare amount
- Total amount

Both average and median values were used to understand the typical values in the dataset.

### 2. Trip Analysis

Analyzed:

- Trip distance distribution
- Trip duration distribution

Trips were grouped into ranges to understand the most common trip distances and durations.

### 3. Time Analysis

Analyzed taxi demand by:

- Pickup date
- Day of the week
- Pickup hour

For weekday analysis, average trips per day were calculated to compare the weekdays.

### 4. Payment Analysis

Analyzed:

- Number of trips by payment type
- Average fare amount by payment type
- Average total amount by payment type
- Trip share by payment type

### 5. Location Analysis

The cleaned trip data was joined with the NYC Taxi Zone lookup table.

Analyzed:

- Top pickup zones
- Top drop-off zones
- Top pickup and drop-off routes

### 6. Anomaly Analysis

Trips with durations above 300 minutes were identified as potential anomalies.

These records were reviewed using trip duration, trip distance, fare amount, total amount and payment type.

The unusual records were retained because an unusual value does not automatically mean that the record is incorrect.

## Charts

The following charts were created in Excel:

1. Trip Distance Distribution
2. Trip Duration Distribution
3. Trips by Pickup Hour
4. Average Trips per Day by Weekday
5. Payment Type Distribution
6. Top 10 Pickup Zones

## Key Findings

- About 69.1% of trips were 3 miles or less.
- About 88.59% of trips were completed within 30 minutes.
- The highest pickup volume was recorded at 6 PM with 265,569 trips, while 4 AM had the lowest with 28,672 trips.
- Saturday had the highest average daily trip volume at 134,427 trips per day, while Sunday had the lowest at 93,409 trips per day.
- Payment types 1 and 0 together accounted for 89.61% of cleaned trips.
- Upper East Side South had the highest pickup count with 160,343 trips.
- 1,432 trips lasted more than 300 minutes, including 167 trips with zero recorded distance. These were retained as potential anomalies.

## Project Structure

```text
SWYNEX-NYC-Taxi-Exploratory-Data-Analysis/
│
├── 01_SQL/
│   ├── 01_Overall_Statistics.sql
│   ├── 02_Time_Analysis.sql
│   ├── 03_Trip_Analysis.sql
│   ├── 04_Payment_Analysis.sql
│   ├── 05_Location_Analysis.sql
│   └── 06_Anomaly_Analysis.sql
│
├── 02_Data/
│   └── Cleaned_Data_Sample.csv
│
├── 03_Charts/
│   ├── 01_Trip_Distance_Distribution.png
│   ├── 02_Trip_Duration_Distribution.png
│   ├── 03_Trips_by_Pickup_Hour.png
│   ├── 04_Average_Trips_per_Day_by_Weekday.png
│   ├── 05_Payment_Type_Distribution.png
│   └── 06_Top_10_Pickup_Zones.png
│
├── 04_Results/
│   └── EDA_Insights.md
│
├── 05_Documentation/
│   ├── 01_EDA_Approach.md
│   └── 02_Analysis_Notes.md
│
└── README.md
```

## Dataset Sample

The `02_Data` folder contains a 10,000-row sample of the cleaned dataset for reference.

The complete cleaned dataset contains 3,724,777 records and was analyzed in Snowflake.

The 10,000-row file is only a sample and does not represent the complete dataset.

## Outcome

This analysis helped me understand the main patterns in the NYC taxi data, including trip distance and duration, demand by time and weekday, payment distribution, high-activity locations and unusual long-duration records.

The results were summarized through SQL analysis, Excel charts and documented findings.

## Internship

**SWYNEX Technologies - Data Analytics Internship**

**Task 2: Exploratory Data Analysis**