# Prediction of Taxi fares  - Educational ML Project
## Overview
This project is a **didactic exercise** focused on exploring, training, and evaluating **different Machine Learning models** to predict taxi fare prices based on a variety of input features such as distance, trip duration, traffic, time of day, and weather conditions.

------
## Objectives

- Understand and apply data preprocessing techniques (handling missing values, encoding categorical features, etc.)
- Perform exploratory data analysis (EDA)
- Train and evaluate different regression models (e.g., Linear Regression, Support Vector Machines, Random Forest)
- Use feature engineering to improve model performance
---

## Dataset Summary

The dataset includes **1,000 taxi trip records** with the following features:

- `Trip_Distance_km`: Distance of the trip (numerical)
- `Trip_Duration_Minutes`: Duration of the trip (numerical)
- `Time_of_Day`: Categorical (Morning, Afternoon, Evening, Night)
- `Day_of_Week`: Categorical (Weekday, Weekend)
- `Traffic_Conditions`: Categorical (Low, Medium, High)
- `Weather`: Categorical (Clear, Rain, Snow)
- `Passenger_Count`: Number of passengers (numerical)
- `Base_Fare`, `Per_Km_Rate`, `Per_Minute_Rate`: Fare structure details
- `Trip_Price`: Target variable (fare amount in USD)

The dataset contains also missing values and outliers, providing the opportunity to face data cleaning challenges.
This dataset is designed to predict taxi trip fares based on various factors such as distance, time of day, traffic conditions, and more. It provides realistic synthetic data for regression tasks, offering a unique opportunity to explore pricing trends in the taxi industry.

## Project Structure

The project includes the following files and folders, organized by type and purpose:

- Taxi_trip_pricing (csv): Dataset containing the original taxi trip pricing data.
- Data_cleaning (code for cleaning): Code used for cleaning and transforming the original dataset, including handling missing values and normalization.
- Data_clean (csv): Dataset resulting from data cleaning and preprocessing, ready for modeling.
- Linear_model_taxi (code): Code implementing linear models for prediction based on taxi trip data. It contains also feature selection procedures such as best subset selection. 
- SVM_taxi (code): Code implementing the Support Vector Machine (SVM) model for analyzing and predicting taxi trip data. Particularly: SVR with parameters found by Cross Validation.
- Decision_Trees_taxi (code): Code for building and training Decision Tree models applied to taxi trip data. Including Cost Complexity Pruning and Gradient Boosting. 

# Conclusion
If we focus only on prediction performance, the Support Vector Regression with a non-linear kernel is the best one with an accuracy of 99.46%

In this scenarion, we can conclude that **non-linear models handle categorical variables better**.
In linear models, categorical variables were often not significant unless interaction terms were introduced between them. Nonlinear models, on the other hand, can automatically capture these relationships without the need to manually create new terms.

Compared with linear regression, nonlinear models (such as Decision Trees, Random Forests, or SVMs with nonlinear kernels) performed better, however, **they are more difficult to interpret**.

