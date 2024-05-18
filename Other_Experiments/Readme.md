# Bitcoin Close Price Prediction
This folder contains four experiments other than our main aproach that is focused on predicting Bitcoin's close price using various methods: Technical Analysis, ARIMA, VAR (Vector AutoRegression), and Anomaly Detection.

## Table of Contents
### Introduction
#### Experiments
- **Technical Analysis**
- **ARIMA** (AutoRegressive Integrated Moving Average)
- **VAR** (Vector AutoRegression)
- **Anomaly Detection**

In this project, we explore different methodologies to predict the close price of Bitcoin. The four experiments conducted are:

Technical Analysis
ARIMA (AutoRegressive Integrated Moving Average)
VAR (Vector AutoRegression)
Anomaly Detection
Experiments
Technical Analysis
Technical analysis involves using historical price and volume data to forecast future price movements. In this experiment, we used various technical indicators such as moving averages, RSI (Relative Strength Index), and MACD (Moving Average Convergence Divergence).

Folder: technical_analysis
Key Files: technical_analysis.ipynb, indicators.py
ARIMA (AutoRegressive Integrated Moving Average)
ARIMA is a popular time series forecasting method that uses past values to predict future values. We optimized the parameters (p, d, q) to build the best model for Bitcoin close price prediction.

Folder: arima
Key Files: arima_model.ipynb, arima_forecast.py
VAR (Vector AutoRegression)
VAR models multivariate time series data and captures the linear interdependencies among multiple time series. We applied VAR to Bitcoin prices and other related financial metrics.

Folder: var
Key Files: var_model.ipynb, var_analysis.py
Anomaly Detection
Anomaly detection aims to identify unusual data points that do not fit the general pattern. We used methods like Isolation Forest and Local Outlier Factor to detect anomalies in Bitcoin price data.

Folder: anomaly_detection
Key Files: anomaly_detection.ipynb, anomaly_methods.py
Results
A summary of the results from each experiment is provided below. For detailed results and analysis, refer to the respective Jupyter Notebooks and scripts in each experiment's folder.

Technical Analysis: Identified key support and resistance levels, and provided buy/sell signals based on technical indicators.
ARIMA: Achieved a satisfactory level of prediction accuracy with optimized parameters (p, d, q).
VAR: Successfully modeled the interdependencies between Bitcoin price and other financial indicators, leading to improved forecast accuracy.
Anomaly Detection: Effectively detected anomalies in the price data which could signify potential market shifts or irregular trading activity.
