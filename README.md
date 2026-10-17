# Car Price Prediction

## Project Overview

This project builds regression models to predict used-car selling prices from vehicle characteristics, including year, present price, kilometers driven, fuel type, seller type, transmission, and previous owners. It was completed as part of the CodeAlpha Data Science Internship.

## Objectives

- Explore and visualize used-car data.
- Prepare numerical and categorical features.
- Train and compare regression models.
- Evaluate models using MAE, RMSE, and R².
- Identify the best-performing model.

## Dataset

`Car_Price.csv` contains 301 rows and nine columns: `Car_Name`, `Year`, `Selling_Price`, `Present_Price`, `Driven_kms`, `Fuel_Type`, `Selling_type`, `Transmission`, and `Owner`. There are no missing values. `Selling_Price` is the target. `Car_Name` is excluded from predictive features because it contains many unique categories.

## Technologies Used

Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, and Jupyter Notebook.

## Methodology

1. Load the dataset and explore price distributions, correlations, and categorical variables.
2. Select vehicle characteristics as features and `Selling_Price` as the target.
3. Split the data into 80% training and 20% testing with `random_state=42`.
4. Use one-hot encoding for categorical variables with `OneHotEncoder(handle_unknown="ignore")`.
5. Train Linear Regression, Decision Tree Regressor, and Random Forest Regressor models.
6. Compare MAE, RMSE, and R².
7. Plot actual versus predicted prices.

## Model Performance

| Model                   |        MAE |       RMSE |   R² Score |
| ----------------------- | ---------: | ---------: | ---------: |
| Linear Regression       |     1.2164 |     1.8658 |     0.8489 |
| Decision Tree Regressor |     0.7234 |     1.1215 |     0.9454 |
| Random Forest Regressor | **0.6146** | **0.9193** | **0.9633** |

_Error metrics are expressed in the target variable's price units._

Random Forest Regressor performed best on the test set, with an MAE of 0.6146, RMSE of 0.9193, and R² of 0.9633. This R² indicates that the model explains approximately 96.33% of the variation in selling prices in this test sample.

## Results

Model comparison results are saved in `results/model_comparison.csv`. The notebook includes exploratory visualizations, preprocessing, model training, evaluation, and an actual-versus-predicted plot.

## Conclusion

Random Forest Regressor achieved the lowest prediction errors and the highest R² score among the three evaluated models on the test set.

## Author

**EBENEZER DABIRE**  
GitHub: https://github.com/EBEN-DATASCIENTIST1
