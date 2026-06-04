# Energy Consumption Time Series Forecasting

## Project Overview

This project focuses on forecasting short-term household energy consumption using historical power usage data. The objective is to analyze time-based consumption patterns and compare the performance of different forecasting approaches, including statistical, machine learning, and specialized time-series models.

The project implements:

* ARIMA (Statistical Forecasting)
* Prophet (Time-Series Forecasting)
* XGBoost (Machine Learning Forecasting)

The models are evaluated using MAE and RMSE metrics, and their forecasts are compared against actual energy consumption values.

---

## Problem Statement

Accurate energy consumption forecasting is essential for efficient energy management, demand planning, and resource optimization. Household energy usage often exhibits daily and weekly patterns that can be leveraged to predict future consumption.

This project aims to:

* Forecast short-term household energy usage.
* Identify temporal consumption patterns.
* Compare forecasting model performance.
* Visualize actual versus predicted energy consumption.

---

## Dataset

### Household Power Consumption Dataset

The dataset contains household electric power consumption measurements recorded over time.

### Key Features

| Feature               | Description                  |
| --------------------- | ---------------------------- |
| Date                  | Observation date             |
| Time                  | Observation time             |
| Global_active_power   | Total active power consumed  |
| Global_reactive_power | Reactive power consumed      |
| Voltage               | Voltage measurement          |
| Global_intensity      | Current intensity            |
| Sub_metering_1        | Kitchen energy usage         |
| Sub_metering_2        | Laundry energy usage         |
| Sub_metering_3        | Climate control energy usage |

### Target Variable

* Global_active_power

---

## Project Workflow

### 1. Data Preprocessing

* Load dataset
* Parse Date and Time columns
* Create Datetime index
* Convert target variable to numeric format
* Handle missing values
* Resample minute-level observations into hourly data

### 2. Feature Engineering

Created time-based features:

* Hour
* Day
* Month
* Weekday
* Weekend Indicator
* Lag Features (Lag_1, Lag_24)
* Rolling Mean (24-hour moving average)

### 3. Exploratory Data Analysis (EDA)

Performed:

* Energy consumption trend analysis
* Hourly consumption analysis
* Seasonal pattern identification
* Time-series visualization

### 4. Forecasting Models

#### ARIMA

A traditional statistical forecasting model used for capturing trends and temporal dependencies.

#### Prophet

A forecasting framework designed to handle trend and seasonality effectively.

#### XGBoost

A machine learning model that leverages engineered time-based features to capture complex consumption patterns.

### 5. Model Evaluation

Models were evaluated using:

* MAE (Mean Absolute Error)
* RMSE (Root Mean Squared Error)

Lower values indicate better forecasting performance.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-Learn
* Statsmodels
* Prophet
* XGBoost

---

## Results

The forecasting models were compared using MAE and RMSE metrics.

Typical observations:

* XGBoost achieved the highest forecasting accuracy.
* Prophet effectively captured seasonal patterns.
* ARIMA provided a strong statistical baseline.

---

## Visualizations

The project includes:

* Energy consumption trend plots
* Hourly average consumption plots
* Actual vs Forecasted comparison charts
* Model performance comparison visualizations

---

## Key Insights

* Household energy consumption follows clear hourly patterns.
* Energy usage generally peaks during evening hours.
* Feature engineering significantly improves forecasting accuracy.
* Machine learning models outperform traditional methods in capturing complex patterns.
* Forecasting can support smarter energy planning and consumption management.

---

## Future Improvements

* Hyperparameter tuning for all models.
* Incorporate weather and temperature data.
* Implement LSTM and deep learning forecasting models.
* Deploy the forecasting system as a web application.

---

## Author

**Rasheed Ahmad**

Data Science & Machine Learning Enthusiast

Passionate about transforming data into actionable insights through analytics, machine learning, and forecasting solutions.
