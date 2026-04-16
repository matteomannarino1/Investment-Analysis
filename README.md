# Investment Fund Analysis — Predictive Modeling & Clustering

This project analyses the historical performance of an investment fund using Python, Jupyter Notebook, and machine learning techniques.  
The dataset contains more than 600 observations with daily values of the fund, including price, returns, and derived indicators.

The goal is to:
- clean and preprocess the dataset  
- create lag features and moving averages  
- build predictive models  
- perform clustering to identify market regimes  
- visualize and interpret the results  


## Project Structure
project-folder/
│
├── data/
│   └── fondo.xlsx
│
├── investments.ipynb
└── README.md




## Data Cleaning & Feature Engineering
The dataset includes the following columns:
* date
* n_shares
* purchase_value
* counter_value
* var_pct
* var_euro
* share_price
* daily_return

Additional features:
* share_price_lag1, share_price_lag5
* daily_return_lag1
* ma5, ma20 (moving averages)
* share_price_next5, daily_return_next5, direction_next5

Rows with daily_return = 0 (weekend duplicates) were removed, except for the first observation.

## Machine Learning Models
1. Predictive Models

The following models were tested:
- Linear Regression
- Random Forest Regressor

However, due to the nature of financial time series, predicting the fund value 5 days ahead produced low performance.

2. Classification Model

A Random Forest Classifier was used to predict:
* whether the fund price will go up (1) or down (0) after 5 days.

# Clustering Analysis
K-Means clustering was applied to identify different market regimes based on:
* price levels
* daily returns
* lagged values
* moving averages
* percentage and euro variations

Cluster Interpretation is provided within the code


# Visualizations
The notebook includes:
- time series plots
- correlation heatmaps
- cluster scatterplots
- confusion matrix for classification


# Notes
This is a first draft of the project - new updates will be provided soon.
The project is for educational and analytical purposes only.
Predictions are not intended as financial advice.

