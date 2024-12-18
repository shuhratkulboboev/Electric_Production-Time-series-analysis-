# Electric Production Time Series Forecasting

This project involves analyzing and forecasting electric production data. The dataset was initially non-stationary and was made stationary through various transformations. Two forecasting models were built and compared to evaluate their performance.

---

## Dataset Description

- **Name**: Electric Production Dataset
- **Type**: Time Series
- **Frequency**: Monthly
- **Features**: Single variable representing electric production over time.

---

## Objectives

1. **Stationarity Check**:
   - Determine if the dataset is stationary using:
     - Augmented Dickey-Fuller (ADF) Test
     - Mean and Standard Deviation Trends

2. **Stationarity Transformation**:
   - Apply transformations to make the dataset stationary:
     - Log Transformation
     - Difference Transformation
     - Subtracting the Rolling Mean

3. **Forecasting**:
   - Build and compare two models for forecasting:
     - **ARIMA (AutoRegressive Integrated Moving Average)**
     - **SARIMA (Seasonal ARIMA)**

---

## Methods

### **1. Stationarity Check**
- **ADF Test**: Checks if the null hypothesis (data is non-stationary) can be rejected.
- **Mean and STD Trends**: Observes if the mean and standard deviation change over time.

### **2. Stationarity Transformation**
- **Log Transformation**: Reduces scale differences in the dataset.
- **Difference Transformation**: Removes trends.
- **Subtracting the Rolling Mean**: Detrends the data by subtracting the rolling average.

### **3. Forecasting Models**
- **ARIMA Model**:
  - Suitable for non-seasonal time series.
  - Parameters: `(p, d, q)` determined through grid search.
- **SARIMA Model**:
  - Extends ARIMA to handle seasonality.
  - Parameters: `(p, d, q) × (P, D, Q, s)`.

---

## Results

1. **Stationarity Transformation**:
   - Original dataset was non-stationary.
   - After applying transformations, stationarity was achieved (validated with ADF Test).

2. **Forecasting**:
   - Both models performed well, with the SARIMA model showing slightly better accuracy in handling seasonality.


