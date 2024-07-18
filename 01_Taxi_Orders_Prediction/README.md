# Taxi Orders Prediction

**Project:** Develop a machine learning model that accurately predicts the number of airport taxi orders each hour.

<div align="center">
    <img alt="taxi" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/629219628ed9c708966eb48ee30c936865a7d84b/01_Taxi_Orders_Prediction/Photos/taxi_airport.jpg">
</div>

<br>

## Business Problem

Sweet Lift Taxi company has collected historical data on taxi orders at airports. To attract more drivers during peak hours, they need to predict the amount of taxi orders for the next hour. To do this they need an accurate machine learning model for such a prediction. The company has specified that the RMSE metric on the test set should not be more than 48.

**Data:** The data is stored in file `taxi.csv`. The data contains time series data from 2018 in the form of the number of taxi cab orders received every 10 minutes. The number of orders is in the '*num_orders*' column.

**Solution Steps:**

1. Download the data and resample it by one hour.
2. Analyze the data.
3. Create new features useful in model training.
4. Train different models with different hyperparameters. The test sample should be 10% of the initial dataset. 
5. Test the data using the test sample.
6. Select the model with the best performance on the test dataset.

## Solution Strategy

**Step 1: Data Description and Cleaning**
 In this first section the data is collected and studied. The missing values are estimated or removed. Finally, a initial data description is carried out to get a feel for the data.

**Step 2: Exploratory Data Analysis**
The time series data is analyzed. The mean and standard deviation are calculated. A test is carried out to determine whether the time series is stationary. Trends and seasonality are displayed using the scipy library.

**Step 3: Feature Engineering**
Features useful for time series forecasting are created such as lags, rolling means and datetime data (months, etc.).

**Step 4: Machine Learning Modeling**
Before training, the data must be scaled and split into train, validation and test sets. Then, each model is fitted to the training data and hyperparameters are tuned.

**Step 5: Model Testing**
The trained models are used to make predictions. The RMSE score for each model is recorded. The predicted and actual test values are overlaid in a line plot for an intuitive understanding of how close the model predictions are to the actual values.

**Step 6: Model Selection**
The model with the lowest RMSE score is selected for use in predicting taxi order volume by hour.

## Time Series Trends and Seasonality

**Rolling Mean:**

<div align="center">
    <img alt="timeseries" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/6ada52f556bea8fdc71e1176bd90d2832c5d4cfe/01_Taxi_Orders_Prediction/Photos/ts1.png">
</div>

- Upon visual inspection, the series appears to be mostly stationary since the mean remains fairly constant. Using the adfuller test and receiving a p-value less than 0.05 confirms this. Since the series is stationary, there is no need to take the difference.

- Plotting the original data with the rolling mean supports the result of the adfuller test. The mean remains relatively stable through the series.

**Trend and Seasonality:**

<div align="center">
    <img alt="trendseason" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/791035fb307c5492f07f189a22e239b480728219/01_Taxi_Orders_Prediction/Photos/vg7.png">
</div>

- To study the series in more detail, only 1 month is included in the data slice.
  
- As would be expected, there is a daily seasonal cycle of orders (orders for taxi service are highest at the busiest times of day.
  
- Each week there are 2-3 'humps' of upward/downward trends.

## Machine Learning Applied

#### Dummy Model (Median)

<div align="center">
    <img alt="dummy" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/6ada52f556bea8fdc71e1176bd90d2832c5d4cfe/01_Taxi_Orders_Prediction/Photos/ts2.png">
</div>

|  RMSE  |
|:------:|
| 87.242 | 

#### Linear Regression

<div align="center">
    <img alt="linear" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/6ada52f556bea8fdc71e1176bd90d2832c5d4cfe/01_Taxi_Orders_Prediction/Photos/ts3.png">
</div>

|  RMSE  |
|:------:|
| 52.733 | 

#### Random Forest Regressor

<div align="center">
    <img alt="forest" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/6ada52f556bea8fdc71e1176bd90d2832c5d4cfe/01_Taxi_Orders_Prediction/Photos/ts4.png">
</div>

|  RMSE  |
|:------:|
| 52.733 | 

#### Gradient Boosting Regressor

<div align="center">
    <img alt="gb" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/6ada52f556bea8fdc71e1176bd90d2832c5d4cfe/01_Taxi_Orders_Prediction/Photos/ts5.png">
</div>

|  RMSE  |
|:------:|
| 44.128 | 

#### Autoregressive Model

<div align="center">
    <img alt="ar" src="https://github.com/nelsonj1614/Data_Projects_TripleTen/blob/6ada52f556bea8fdc71e1176bd90d2832c5d4cfe/01_Taxi_Orders_Prediction/Photos/ts6.png">
</div>

|  RMSE  |
|:------:|
| 74.854 | 
