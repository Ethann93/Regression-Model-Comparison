
# Regression Model Comparison and Hyperparameter Tuning

This repository contains Python code for performing regression analysis on a dataset of car attributes to predict fuel efficiency (mpg). The analysis includes data preprocessing, the evaluation of multiple regression models, and hyperparameter tuning to identify the best-performing model. The goal of this project is to combine multiple regression model with stacking regressor in order to create a meta-regression and alternativelty more accurate results.

## Dataset

The dataset used in this project is the "mpg" dataset, which contains information about various car attributes and their fuel efficiency (mpg) as the target variable.

## Stages of the Code

The code is structured as follows:

### 1. Data Preprocessing

- Data Cleaning: The 'name' column, which was irrelevant to the analysis, is dropped.
- Data Encoding: Binary numbers are encoded as categorical columns.
- Handling Missing Values: Six missing values in the 'horsepower' column are replaced with the mean value of 104.47.

### 2. Model Selection and Evaluation

The following regression models are evaluated based on two key metrics: Mean Squared Error (MSE) and R-squared (R²).

- Linear Regression
- Random Forest Regressor
- Ridge Regression
- Gradient Boosting Regression
- Stacking Regressor
- Voting Regressor

The code computes and compares the MSE and R² scores for each model to determine their performance. The best model, based on these metrics, is selected.

### 3. Best Model Selection

Among the evaluated models, the Random Forest Regressor is identified as the best-performing model based on its low MSE and high R² score.

### 4. Hyperparameter Tuning

Hyperparameter tuning is performed on a Stacking Regressor that combines Ridge, Gradient Boosting, Support Vector Regressor, and Random Forest Regressor models. RandomizedSearchCV is used to identify the best hyperparameters to improve the model's performance.

### 5. Final Model Performance

After hyperparameter tuning, the Stacking Regressor exhibits improved MSE and overall predictive accuracy.

## Conclusion

In conclusion, this project demonstrates how to preprocess data, evaluate multiple regression models, select the best-performing model, and perform hyperparameter tuning to further enhance model performance. The Random Forest Regressor is identified as the best model for predicting fuel efficiency, and the hyperparameter-tuned Stacking Regressor may also be a valuable choice in certain scenarios.

Please refer to the Jupyter Notebook or Python script for the complete code and detailed implementation.

## How to Use

1. Clone the repository to your local machine.
2. Run the Jupyter Notebook or Python script to execute the code.
3. Follow the code comments and documentation for a detailed explanation of each stage.

Feel free to adapt and use this code for your own regression analysis projects.

## Dependencies

The code relies on the following Python libraries:

- pandas
- seaborn
- scikit-learn

Ensure that these libraries are installed before running the code.


