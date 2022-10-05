# Covid-19 Forecasting

Forecasting Covid-19 cases using deep learning and statistical models for few
countries.

## Objectives

Our main objective is to see which one of our chosen 4 countries have handled
the virus in a way that can be generalized to everyone as simple guidelines, the
targeted countries are

- United States
- Germany
- Italy
- South Korea
- Malaysia

## Data

The dataset is from our world in data
[GitHub repository](https://github.com/owid/covid-19-data/tree/master/public/data),
it contains daily cases for all countries

## Models

for the modeling, 3 differernt models are trained and compared

- Bidrectional Long Short Term Memory (BiLSTM)
- Autoregressive Integrated Moving Average (ARIMA)
- Holt's Exponential Smoothing (HES)

The statistical models are trained in incremental fashion as defined below:

- train with original train data
- predict the next value
- append the prediction value to the training data
- repeat training and appending for n times (days in this case)

This incremental technique significantly improves the accuracy by always using
all data up to previous day for predicting next value unlike predicting multiple
values at the same time which is not incremental.

## Notebook content

There are 2 notebooks in this project, one for the first 4 countries and another
separate notebook for Malaysia data analysis, the Malaysia notebook answers
questions of different types of analysis (descriptive, diagnostic, predictive
and prescriptive).

- Data Exploration
- Visual and Descriptive Analysis
- Modeling
- Analysis of Effectiveness of mandated lockdown
- Conclusion
