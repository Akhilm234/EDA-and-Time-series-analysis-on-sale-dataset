# EDA-and-Time-series-analysis-on-sale-dataset
This Python script performs sales data analysis and forecasting using time series techniques.  It covers the following steps:

1.  **Data Loading and Cleaning:** Loads sales data from a CSV file, inspects data types and missing values, and removes columns with excessive missing data.  Converts the 'ORDERDATE' column to datetime and sets it as the index.

2.  **Exploratory Data Analysis (EDA):**
    *   Identifies and visualizes the top 20 customers and countries by sales revenue using bar charts.
    *   Analyzes sales distribution across different product lines using a pie chart.

3.  **Time Series Preprocessing:**
    *   Resamples the sales data daily, calculating the mean sales for each day.
    *   Handles any missing values introduced by resampling using linear interpolation.
    *   Splits the time series data into training, testing, and validation sets.

4.  **Stationarity Testing:** Performs the Augmented Dickey-Fuller (ADF) test to determine if the time series is stationary.  Prints the test results and interprets them.

5.  **Time Series Decomposition:** Decomposes the time series into its trend, seasonality, and residual components to better understand underlying patterns.

6.  **SARIMA Model Selection and Fitting:**
    *   Explores a range of parameter combinations for the Seasonal ARIMA (SARIMA) model, considering seasonality with a period of 12 (likely representing monthly seasonality).
    *   Calculates the Akaike Information Criterion (AIC) for each model to identify the best-performing one.
    *   Fits the SARIMA model with the selected optimal parameters.

7.  **Model Diagnostics:** Plots diagnostic charts to assess the model's residuals and ensure that the model assumptions are met.

8.  **Forecasting and Evaluation:**
    *   Generates one-step-ahead forecasts and calculates the Root Mean Squared Error (RMSE) to evaluate forecast accuracy.
    *   Plots the observed sales data along with the forecasted values and confidence intervals.
    *   Produces a 7-day sales forecast and saves it to a CSV file ("prediction.csv").
    *   Plots the forecasted values.

The script utilizes libraries like pandas for data manipulation, matplotlib for visualization, statsmodels for time series analysis (including the ADF test, decomposition, and SARIMA modeling), and scikit-learn for calculating RMSE.  The primary goal is to build a SARIMA model to accurately forecast future sales based on historical data.

