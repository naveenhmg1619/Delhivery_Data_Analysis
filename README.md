# Delhivery Data Analysis Project

## Overview
This project involves a comprehensive analysis of Delhivery's logistics data to extract meaningful insights and provide business recommendations. Delhivery is India's largest and fastest-growing fully integrated logistics services player by revenue in Fiscal 2021.

## Objective
The goal is to leverage feature engineering and data analysis techniques to understand and process data from Delhivery's engineering pipelines, aiding the data science team in building forecasting models.

## Techniques
- Feature Creation
- Column Normalization/Standardization
- Handling Categorical Values
- Missing Values and Outlier Treatment
- Hypothesis Testing
- Visual Analysis

## Tools and Libraries
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn

## Challenges Faced
During the analysis of Delhivery's logistics data, several challenges were encountered:

1. **Data Complexity:** The dataset contained multiple entries for single deliveries, akin to connecting flights, which complicated the aggregation process.
2. **Missing Values:** There were instances of missing data, particularly in the `source_name` and `destination_name` fields.
3. **Outliers:** The dataset exhibited outliers in almost all numerical variables, which could skew the analysis.
4. **Categorical Data Handling:** The dataset included categorical variables that required encoding for proper analysis.
5. **Estimation Discrepancies:** Differences between OSRM estimations and actual measurements needed to be addressed.

## Methods Used
To overcome these challenges, the following methods were employed:

1. **Data Aggregation:** Utilized `groupby` and aggregation functions like `sum()` and `cumsum()` to merge rows based on `Trip_uuid`, `Source ID`, and `Destination ID`.
2. **Handling Missing Values:** Rows with missing `source_name` and `destination_name` were dropped to maintain data integrity.
3. **Outlier Treatment:** Implemented the Interquartile Range (IQR) method to identify and handle outliers.
4. **Categorical Encoding:** Performed one-hot encoding on categorical variables such as `route_type`.
5. **Normalization/Standardization:** Applied `MinMaxScaler` and `StandardScaler` to normalize numerical features.

## Key Insights
1. **High Traffic Routes:** Delhi-Haryana and Mumbai City-Bhiwandi are the busiest routes.
2. **Stable Trip Counts:** Trips remain consistent, with a notable decrease in late September.
3. **State Focus:** Maharashtra and Karnataka are pivotal in trip origins and destinations.
4. **Route Type Analysis:** FTL deliveries cover more distance than carting type deliveries.
5. **Speed Consistency:** FTL delivery speeds are consistent, while carting varies throughout the month.
6. **Distance and Time Discrepancy:** OSRM estimations differ from actual measurements.
7. **Interstate Stops:** The highest number of stops occur between Tamil Nadu-Pondicherry and Assam-Arunachal Pradesh.

## Business Recommendations
1. **Optimize Routes:** Improve efficiency on high-traffic routes.
2. **Analyze Trip Decrease:** Investigate the cause behind the drop in trips in late September.
3. **Focus on Key States:** Allocate resources and plan expansions in Maharashtra and Karnataka.
4. **Improve Estimations:** Enhance algorithms for distance and time predictions.
5. **Examine Stop Locations:** Identify issues and streamline processes on complex routes.

## Conclusion
The analysis provides actionable insights that can help Delhivery optimize its operations and maintain its lead in the logistics sector. By focusing on route optimization, investigating trip fluctuations, and improving estimation accuracy, Delhivery can enhance its service quality and operational efficiency.
