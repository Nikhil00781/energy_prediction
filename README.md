Energy Consumption Analysis and Forecasting
This repository contains a comprehensive analysis and predictive modeling project for energy consumption data. The project explores temporal patterns in energy usage and implements both statistical and machine learning models to forecast future demand.

📊 Project Overview
The primary goal of this project is to analyze historical electricity consumption data (in MWh) and build models capable of predicting future consumption. Accurate energy forecasting is critical for grid management, infrastructure planning, and operational efficiency.

📁 Dataset Description
The analysis is based on the Predicting Energy Consumption.xlsm dataset, which includes:

Start time UTC: The beginning of the recorded hour.

End time UTC: The end of the recorded hour.

Electricity consumption (MWh): The total energy consumed during that hour (Target Variable).

🛠️ Key Features & Preprocessing
To improve model accuracy, several temporal features were engineered from the UTC timestamps:

Hour of Day: Captures daily consumption cycles (e.g., peak business hours).

Day of Week: Identifies differences between weekday and weekend usage.

Month: Captures seasonal variations throughout the year.

Is Weekend: A binary flag for Saturday and Sunday.

Lag Features: Includes lag_1h (previous hour) and lag_24h (same hour previous day) to capture autocorrelation in the time series.

🔍 Exploratory Data Analysis (EDA)
The notebook performs detailed EDA to visualize energy trends:

Time Series Plots: Visualizing overall consumption over time.

Boxplots: Analyzing consumption distribution by hour of the day and day of the week to identify peak demand periods.

Correlation Analysis: Using heatmaps to understand the relationship between engineered features and energy demand.

🤖 Modeling Approach
The project compares traditional statistical methods with modern machine learning techniques:

Baseline (Naive) Model: Uses the previous hour's consumption as the prediction for the current hour.

ARIMA: A statistical time-series model (AutoRegressive Integrated Moving Average) used for walk-forward validation.

Random Forest Regressor: A machine learning ensemble method that significantly outperformed the baseline by capturing non-linear patterns.

Performance Results
The Random Forest model demonstrated superior performance:

Random Forest RMSE: ~120.71 MWh

Baseline RMSE: ~238.08 MWh

Improvement: The ML approach reduced error by approximately 49% compared to the naive baseline.
