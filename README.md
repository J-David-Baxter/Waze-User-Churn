# Predicting Waze User Churn

## Overview
The goal of this project was to build a machine learning model to predict user churn for Waze. The project used a sample of Waze user data. We used an ensemble of tree-based machine learning models and a logistic regression model to predict user churn. The best model was an XGBoost model, with an F1 score of ~23% and a recall score of ~16%. Based on the results, the data team concluded that the current data is not sufficient to build a reliable model that predicts user churn. There is a critical need for more data in order to make a model that can be used to drive business decisions. 

## Business Understanding
Waze leadership is looking to improve their app and expand their user base. They want to increase overall growth by limiting monthly user churn. A good predictive model will help Waze to identify users at risk of churning and proactively engage with them to increase overall user retention.

## Data Understanding
The Waze user data has 15,000 rows and 13 columns. Features include number of sessions, total number of drives, total distance driven, number of days the user used the app, device type, and whether or not the user is still active. The pie chart below shows the split between retained and churned users in the dataset.

![waze pie chart](https://github.com/J-David-Baxter/Waze-User-Churn/assets/57837488/63ee16b3-8951-416d-b94e-ccdf75a05ddb)

## Modeling and Evaluation
The data team built a random forest model and an XGBoost model and evaluated them based on key metrics (accuracy, precision, recall, f1). THe XGBoost model performed the best, with 80.6% accuracy, 38.9% precision, 16.7% recall, and an F1-score of 23.2% when makinig predictions on the test data. We used feature engineering to maximise the performance of the model, since the logistic regression model made earlier in the project performed poorly using the original features. The following chart shows the feature importance based on our final model.

![waze features](https://github.com/J-David-Baxter/Waze-User-Churn/assets/57837488/6ddf817a-c34b-435d-9a1e-4fc6239e326b)

The top 5 features were kilometers per hour, number of days since onboarding, session percent, total sessions per day, and the duration of drives in minutes. 

## Conclusion
The final model is not useful for making predictions or driving business decisions. However, it can be used to drive further exploratory efforts, such as deciding what kind of data needs to be collected to make better models in the future. It would be helpful to have more granular data about how users interact with the app, as well as more detailed driving data like location and time. The data team recommends a second iteration of the user churn project with more data and feature engineering in order to make a useable model.
