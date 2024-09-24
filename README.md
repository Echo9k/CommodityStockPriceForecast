# Commodity Stock Price Forecasting

Our investment fund management team would like to analyze time-series data for stock price forecasting. We'd like to start by predicting the value of stocks, based on historical data, for five commodity-producing companies. Our data scientists will run the forecasting process, but our stock analysts also need to see the data for further study and reporting.

KPIs Targeted:

- Operating Profit 1M+
- Assets Under Management
- Retum On Assets

## Objectives:

- Determine how to use historical stock data and train a long short-term memory network (LSTM) prediction model by using the TensorFlow framework in Amazon SageMaker Studio.
- Determine how to save the resulting stock and predictions data to an Amazon S3 bucket for later consumption.
- Examine how Amazon Athena can be used to confirm that your stock and predictions data is available for users to query.

## AWS services

- AWS Glue
- Amazon S3
- Amazon SageMaker
- Amazon Athena

# Steps

1. This solution ingests historical stock data, trains a predictive model, and saves the resulting predictions to data lake for use by data scientists and stock analysts.
2. Data scientists load and run an Amazon SageMaker notebook application to obtain historical stock data and save it to a data lake in Amazon Simple Storage Service (Amazon S3).
3. The SageMaker notebook calls TensorFlow on AWS to train a long short-term memory (LSTM) predictive model, using the historical stock data, and then saves prediction data to the S3 data lake.
4. AWS Glue access the data lake and discovers the prediction data’s schema which is used to create tables in AWS Glue Data Catalog.
5. Stock analysts access the saved prediction data by running SQL queries though Amazon Athena. The analysts use a dashboard or visualization application that import the query results from Athena.
6. To test the effect on training time, the LSTM model training job’s machine instance size, batch size, and epoch size can be changed.