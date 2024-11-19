+++
date = "2022-11-05T19:41:01+05:30"
title = "Stock Price Prediction using Python and the LSTM Machine Learning Model"
draft = false
image = "img/portfolio/stockmarket.png"
showonlyimage = false
weight = 4
+++


In this project, I used Python and the LSTM machine learning model to predict the stock price of TSLA (Tesla, Inc.). We start by importing the necessary libraries and creating a Ticker object for TSLA. Then visualized the closing price and create a new data frame with only the close column. This data frame is converted to a numpy array and scaled using a MinMaxScaler.

Data is split into training and testing datasets, which are then converted to numpy arrays. An LSTM model is built and compiled, and is then trained on the training data. 

The model is used to make predictions on the testing data, and the performance of the model is evaluated using various evaluation metrics. The results are visualized and the model is used to predict the stock price of TSLA on the next trading day.

Overall, this project demonstrates how machine learning can be used to predict stock prices and provides a step-by-step guide for implementing this approach using Python and the LSTM model.

#### I have used the following libraries in python and installed:

- 	yfinance
-	pandas
-	numpy
-	matplotlib
-	keras

![LSTM Prediction](/img/portfolio/stockmarket.png)