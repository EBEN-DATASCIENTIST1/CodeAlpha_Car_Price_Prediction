# Car Price Prediction

## Project Overview

This project was completed as part of the CodeAlpha Data Science Internship.

The objective is to build regression models that predict car selling prices
using vehicle-related features.

## Dataset

The dataset contains 301 car records and 9 columns.

The target variable is:

- `Selling_Price`

The features used for prediction are:

- `Year`
- `Present_Price`
- `Driven_kms`
- `Fuel_Type`
- `Selling_type`
- `Transmission`
- `Owner`

The `Car_Name` column was excluded because it contains individual car names
with many unique categories.

## Exploratory Data Analysis

The following analyses were performed:

- Distribution of selling prices
- Correlation analysis of numerical features
- Distribution of categorical features

The correlation analysis showed a strong positive relationship between
`Present_Price` and `Selling_Price` in this dataset.

## Data Preprocessing

The categorical features were converted into numerical representations using
One-Hot Encoding.

The dataset was divided into:

- 80% training data
- 20% testing data

## Machine Learning Models

Three regression algorithms were trained and compared:

1. Linear Regression
2. Decision Tree Regression
3. Random Forest Regression

## Model Evaluation

The models were evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

### Results

| Model             |    MAE |   RMSE | R² Score |
| ----------------- | -----: | -----: | -------: |
| Linear Regression | 1.2164 | 1.8658 |   0.8489 |
| Decision Tree     | 0.7234 | 1.1215 |   0.9454 |
| Random Forest     | 0.6146 | 0.9193 |   0.9633 |

The Random Forest model had the strongest observed performance on the
20% test split, with an R² score of 0.9633.

## Visualization

An Actual vs Predicted Prices plot was created to compare the model's
predictions with the actual selling prices.

## Project Structure

text
CodeAlpha_Car_Price_Prediction/
│
├── data/
│ └── Car_Price.csv
│
├── notebooks/
│ └── car_price_prediction.ipynb
│
├── results/
│ └── model_comparison.csv
│
├── README.md
└── requirements.txt
