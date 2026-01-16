# Energy Consumption Prediction Analysis

This repository contains a comprehensive analysis and time-series forecasting project focused on energy consumption data. The goal is to predict electricity demand using historical data through Exploratory Data Analysis (EDA), statistical modeling (ARIMA), and Machine Learning (Random Forest).

## 📊 Project Overview
Energy forecasting is a critical task for grid operators to balance supply and demand. This project walks through the lifecycle of a data science problem: from raw data ingestion to evaluating model performance against a baseline.

## 🗂️ Dataset Description
The analysis uses a time-indexed dataset (`Predicting Energy Consumption.xlsm`) with the following structure:
* **Start Time UTC**: Timestamp indicating the beginning of the consumption window.
* **End Time UTC**: Timestamp indicating the end of the window.
* **Electricity consumption (MWh)**: The target variable (int64) representing hourly energy usage.

## 🛠️ Features
The notebook performs extensive **Feature Engineering** to capture temporal patterns:
* **Calendar Features**: Hour of the day, day of the week, month, and weekend indicators.
* **Lag Features**: Historical values (t-1 and t-24) to provide the model with context from the previous hour and the previous day.

## 🔍 Exploratory Data Analysis (EDA)
The project includes several visualizations to understand the data:
* **Time Series Plots**: To identify overall trends and fluctuations.
* **Boxplots**: To analyze hourly and weekly seasonality (e.g., peak hours vs. off-peak).
* **Correlation Heatmaps**: To see which temporal features most strongly impact energy consumption.

## 🤖 Modeling & Evaluation
The project implements a "Walk-Forward" validation strategy and compares three distinct approaches:

| Model | Description | Purpose |
| :--- | :--- | :--- |
| **Naive Baseline** | Persistence model ($t = t-1$) | Establishes a minimum performance benchmark. |
| **ARIMA** | Statistical AutoRegressive model | Captures linear relationships in the time series. |
| **Random Forest** | Machine Learning Regressor | Captures non-linear patterns and complex interactions. |

### Key Results
* **Baseline RMSE**: ~238.08 MWh
* **Random Forest RMSE**: ~120.71 MWh
* **Performance**: The Random Forest model achieved a **~49% reduction in error** compared to the baseline.

## 🚀 How to Use
1. **Clone the repository**:
   ```bash
   git clone [https://github.com/your-username/energy-prediction.git](https://github.com/your-username/energy-prediction.git)
