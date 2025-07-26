# Time Series Analysis and Forecasting

This project explores various time series datasets to identify patterns, analyze trends and seasonality, and build predictive models using a range of statistical and machine learning techniques.

## Author

Jonah Zembower

## Date

May 6, 2024

## Project Overview

The core objective is to demonstrate proficiency in time series analysis, covering data preprocessing, exploratory data analysis, and the implementation and evaluation of forecasting models. The project investigates different types of time-dependent data to extract meaningful insights and predict future values.

## Datasets

The repository includes the following datasets:

* **`DinosaurPark.txt`**: Monthly ticket sales data for a dinosaur park, spanning from 1992 to 2002.
    * **Key Findings**: The data exhibits a clear seasonal pattern with consistent spikes, alongside an overall upward trend in sales over the years. Sales notably increase in November and December.
* **`electricity_consumption_data.csv`**: Hourly records of electricity consumption.
* **`Sunspots.csv`**: Historical monthly mean total sunspot numbers.
    * **Key Findings**: Seasonal decomposition reveals an 11-year solar cycle, with residuals appearing random.
* **`website_traffic_data.csv`**: Daily website visitor counts.

## Methodologies & Models

The project implements a comprehensive approach to time series analysis:

### Data Preprocessing & Exploration
* **Date Handling**: Conversion of date columns to datetime objects and setting them as DataFrame indices.
* **Missing Values**: Imputation of missing data by replacing them with mean values.
* **Time Series Decomposition**: Deconstruction of time series into trend, seasonal, and residual components to understand underlying patterns.
* **Stationarity Tests**: Application of the Augmented Dickey-Fuller (ADF) test to check for stationarity in the time series.
* **Rolling Statistics**: Calculation and plotting of rolling mean and standard deviation to observe trends and volatility.
* **Data Reshaping**: Custom functions for restructuring time series data into hourly, weekly, and monthly formats for detailed analysis.

### Forecasting Models
* **ARIMA (AutoRegressive Integrated Moving Average)**: Utilized for forecasting, with optimal (p, d, q) orders selected based on AIC and BIC scores.
* **SARIMA (Seasonal ARIMA)**: An advanced model for time series with seasonal components, with seasonal parameters (P, D, Q, s) determined.
* **Holt's Winters Method**: Employed for exponential smoothing, effective for data with both trend and seasonality.
* **Neural Networks (MLP & LSTM)**: Implemented for more complex pattern recognition and forecasting, with performance evaluated through cross-validation. The Neural Network model achieved an Average MSE of 0.00377 and an Average RMSE of 0.06127 on one of the datasets.

### Model Evaluation
* **Mean Absolute Error (MAE)**: Measures the average magnitude of the errors in a set of forecasts.
* **Mean Squared Error (MSE)**: Calculates the average of the squares of the errors.
* **Least Squares Line**: Visualizes the linear trend within the data.

## Improvement Opportunities

Future enhancements could include:

* **Model Complexity**: Exploring more intricate LSTM architectures or additional dense layers.
* **Feature Engineering**: Incorporating new features like prior solar cycle lengths or other relevant indicators to improve predictive power.
* **Hyperparameter Tuning**: Extensive experimentation with learning rates, number of epochs, and batch sizes to optimize model performance.
* **Data Augmentation**: Expanding the dataset through various augmentation techniques to provide more training examples.

## Technologies Used

* **Python**
* **pandas**: For data manipulation and analysis.
* **numpy**: For numerical operations.
* **matplotlib** & **seaborn**: For data visualization.
* **statsmodels**: For time series analysis and statistical modeling (seasonal decomposition, ARIMA, SARIMA, ADF test, exponential smoothing).
* **scikit-learn**: For machine learning metrics and linear regression.
* **pmdarima**: For automated ARIMA model selection.

## Files in the Repository

* `DinosaurPark.txt`: Monthly ticket sales data.
* `electricity_consumption_data.csv`: Hourly electricity consumption data.
* `Sunspots.csv`: Historical sunspot records.
* `website_traffic_data.csv`: Daily website visitor data.
* `Final_Project copy.ipynb`: Jupyter Notebook with the complete data analysis and modeling code.
* `Final Presentation.pptx`: Presentation slides summarizing the project's findings.
* `README.md`: This README file.
