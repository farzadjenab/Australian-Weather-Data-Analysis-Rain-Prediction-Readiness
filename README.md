# Australian Weather Data Analysis: Rain Prediction Readiness

## Project Overview

This project undertakes a comprehensive Exploratory Data Analysis (EDA) of the `weatherAUS.csv` dataset, which contains daily weather observations from various locations across Australia. The primary objective is to understand the dataset's structure, identify data quality issues (especially missing values), analyze the distributions and relationships among weather parameters, and ultimately prepare the data for potential future machine learning model development focused on predicting rainfall.

As a Junior Data Analyst, this analysis demonstrates proficiency in data loading, inspection, cleaning, statistical summarization, and visualization techniques essential for transforming raw data into actionable insights.

## Dataset Description

The `weatherAUS.csv` dataset includes daily weather observations for 49 different locations in Australia. It spans from 2008-12-01 to 2017-06-25, comprising approximately 145,460 records and 23 features.

### Key Features:

*   **Date:** The date of observation.
*   **Location:** The location where the observation was taken.
*   **MinTemp / MaxTemp:** Minimum and maximum temperatures (in Celsius).
*   **Rainfall:** The amount of rainfall recorded for the day (in mm).
*   **Evaporation:** The amount of evaporation (in mm).
*   **Sunshine:** The number of hours of bright sunshine.
*   **WindGustDir / WindGustSpeed:** Direction and speed of the strongest wind gust.
*   **WindDir9am / WindDir3pm:** Wind direction at 9 am and 3 pm.
*   **WindSpeed9am / WindSpeed3pm:** Wind speed at 9 am and 3 pm.
*   **Humidity9am / Humidity3pm:** Humidity at 9 am and 3 pm (in percent).
*   **Pressure9am / Pressure3pm:** Atmospheric pressure at 9 am and 3 pm (in hpa).
*   **Cloud9am / Cloud3pm:** Fraction of sky obscured by cloud at 9 am and 3 pm.
*   **Temp9am / Temp3pm:** Temperature at 9 am and 3 pm (in Celsius).
*   **RainToday:** Boolean: 'Yes' if rainfall (mm) for the day was > 1mm, otherwise 'No'.
*   **RainTomorrow:** The target variable. Boolean: 'Yes' if it rained the next day, otherwise 'No'.

## Project Goals

1.  **Data Loading & Initial Inspection:** Load the dataset and perform initial checks (head, tail, sample, info, shape).
2.  **Missing Value Analysis:** Quantify and visualize the extent of missing data in each column.
3.  **Data Type Validation:** Ensure columns have appropriate data types, especially for 'Date' and categorical variables.
4.  **Descriptive Statistics:** Generate summary statistics for numerical features to understand central tendency, spread, and potential outliers.
5.  **Distribution Analysis:** Visualize the distribution of key numerical features using histograms to identify patterns and anomalies.
6.  **Categorical Variable Analysis:** Examine unique values and frequencies of categorical features using value counts and bar plots.
7.  **Correlation Analysis:** Investigate relationships between numerical features using a correlation matrix and heatmap.
8.  **Feature Engineering (Planned):** Discuss potential feature engineering steps, such as extracting temporal features from 'Date'.
9.  **Data Cleaning & Preprocessing (Planned):** Outline strategies for handling missing values and preparing data for machine learning.

## Tools and Technologies

*   **Python:** Programming language for data analysis.
*   **Pandas:** Data manipulation and analysis library.
*   **NumPy:** Numerical computing library.
*   **Matplotlib:** Data visualization library.
*   **Seaborn:** Enhanced data visualization library.
*   **Jupyter Notebook:** Interactive computing environment for analysis.

## Analysis Steps

The project involves the following detailed steps within a Jupyter Notebook environment:

1.  **Import Libraries:** Essential libraries such as `pandas`, `numpy`, `matplotlib.pyplot`, and `seaborn` are imported.
2.  **Load Dataset:** The `weatherAUS.csv` file is loaded into a pandas DataFrame.
3.  **Basic Data Exploration:**
    *   `df.head()`, `df.tail()`, `df.sample()` to view data examples.
    *   `df.info()` to check data types and non-null counts.
    *   `df.shape` to get dimensions.
    *   `df.columns` to list all column names.
4.  **Missing Values Treatment:**
    *   Calculate and display the count and percentage of `NaN` values per column.
    *   Visualize missing values using a bar chart.
    *   Discuss imputation or removal strategies for future steps.
5.  **Numerical Feature Analysis:**
    *   `df.describe()` for summary statistics.
    *   Histograms with KDE plots for all numerical columns to visualize distributions.
6.  **Categorical Feature Analysis:**
    *   `value_counts()` and `nunique()` for each categorical column.
    *   Bar plots for categorical features with a reasonable number of unique values.
7.  **Correlation Matrix:**
    *   Compute the correlation matrix for all numerical features.
    *   Visualize the correlations using a `seaborn.heatmap`.
8.  **Date Column Transformation:**
    *   Convert the 'Date' column to datetime objects.
    *   Extract 'Year', 'Month', and 'Day' as new features.

## Conclusion

This EDA provides a solid foundation for understanding the Australian weather dataset. It highlights areas requiring further attention, such as significant missing data in several columns (`Evaporation`, `Sunshine`, `Cloud9am`, `Cloud3pm`, `Pressure`, `Humidity`, `WindSpeed`), and reveals the distributions and relationships among various weather variables. The insights gained from this analysis are crucial for informed decisions regarding data preprocessing and feature selection, paving the way for developing robust predictive models for rain forecasting.

## Usage

To run this analysis:

1.  Clone the repository:
bash
git clone https://github.com/farzadjenab/Australian-Weather-Data-Analysis-Rain-Prediction-Readiness
cd  Australian-Weather-Data-Analysis-Rain-Prediction-Readiness

2. Ensure you have the weatherAUS.csv file in the project directory.
3. Install the required Python libraries:

bash

pip install pandas numpy matplotlib seaborn jupyter

4. Open and run the Jupyter Notebook:


bash

## Future Work
1. Implement various strategies for handling missing data (e.g., mean imputation, median imputation, regression imputation, or removal based on analysis).
2. Address outliers identified in numerical features.
3. Further feature engineering (e.g., creating seasonal indicators, interaction terms).
4. Develop and evaluate machine learning models (e.g., Logistic Regression, Random Forest, Gradient Boosting) to predict RainTomorrow.
5. Explore more advanced visualization techniques to uncover deeper insights.
