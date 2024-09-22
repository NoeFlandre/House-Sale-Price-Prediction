# House Price Prediction using Machine Learning 🏡

## Overview

This project focuses on building and tuning various machine learning models to predict house prices based on housing characteristics. Using a dataset from Kaggle, we experimented with multiple machine learning algorithms and evaluated their performance. The ultimate goal is to predict house prices as accurately as possible using models trained on features like square footage, neighborhood, number of rooms, and more.

## Table of Contents

- [Project Overview](#overview)
- [Dataset](#dataset)
- [Features](#features)
- [Modeling](#modeling)
- [Performance Metrics](#performance-metrics)
- [Results](#results)


## Dataset

The dataset is sourced from [Kaggle](https://www.kaggle.com/) and consists of housing data. It includes 81 explanatory variables that describe every aspect of residential homes in Ames, Iowa, and the target variable, `SalePrice`, which is the price of the house.

**Key steps in data processing include**:
- Handling missing values
- Encoding categorical variables (using one-hot encoding and label encoding)
- Feature engineering (e.g., adding house age and total number of bathrooms)
- Removing outliers and addressing skewed distributions

## Features

Some of the key features in the dataset include:
- `OverallQual`: Overall material and finish quality
- `GrLivArea`: Above-ground living area square footage
- `GarageCars`: Size of the garage in terms of car capacity
- `TotalBsmtSF`: Total square feet of basement area
- `1stFlrSF`: First-floor square footage
- `ExterQual`: Exterior material quality

We engineered new features such as `HouseAge`, `RemodelAge`, and `TotalBathrooms` to improve model performance.

## Modeling

We experimented with and fine-tuned several machine learning models:
- **Linear Regression** (including Ridge and Lasso for regularization)
- **K-Nearest Neighbors (KNN)**
- **Support Vector Regression (SVR)**
- **Random Forest**
- **Gradient Boosting**
- **XGBoost**
- **Neural Networks**

### Tuning

We used **GridSearchCV** for hyperparameter tuning, focusing on models such as Gradient Boosting, XGBoost, and Random Forest to optimize their parameters.

## Performance Metrics

The models were evaluated using three main metrics:
- **RMSE (Root Mean Squared Error)**: Measures the square root of the average squared differences between predicted and actual values.
- **MAE (Mean Absolute Error)**: Measures the average magnitude of the errors in a set of predictions.
- **R² (Coefficient of Determination)**: Represents the proportion of the variance in the target variable that is predictable from the independent variables.

## Results

The **Gradient Boosting** and **XGBoost** models performed the best in terms of predictive accuracy, with the lowest **RMSE** and highest **R²** values. Below is a summary of the tuned model performances:

| **Model**                     | **RMSE**    | **MAE**     | **R²**  |
|-------------------------------|-------------|-------------|---------|
| **Tuned Gradient Boosting**    | 25,269.81   | 16,386.60   | 0.91    |
| **Tuned XGBoost**              | 25,697.76   | 16,663.51   | 0.90    |
| **Tuned Neural Network**       | 29,729.76   | 20,700.46   | 0.87    |
| **Tuned Random Forest**        | 31,051.20   | 18,734.83   | 0.86    |
| **Tuned Ridge Regression**     | 30,268.89   | 19,183.92   | 0.87    |
| **Tuned Lasso Regression**     | 30,268.19   | 19,318.46   | 0.87    |

