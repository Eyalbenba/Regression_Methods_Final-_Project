#Airbnb Apartment Pricing Prediction using Logistic Regression

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Key Things That Improved the Model](#key-things-that-improved-the-model)

## Introduction
This project was done as a part of Regression Models Course @ BGU SISE Deptarment.
The project aims to predict whether an Airbnb apartment is expensive or not using logistic regression. The goal is to develop a model that can classify apartments as either expensive or not based on a set of features.

## Dataset
The dataset used for this project consists of two CSV files: train.csv and test.csv. The train.csv file contains the training data, while the test.csv file is used for evaluating the trained model's performance. Each CSV file contains over 50 features related to Airbnb apartments, including location, amenities, number of bedrooms, and more.

## Key Thing That Improved The Model
### Feature Engineering
During the development of our model, we focused on feature engineering to enhance its predictive performance. Two notable improvements we made were:

Location Feature: Initially, we explored the GPS coordinates of the apartments and observed that they were primarily located in Japan. To leverage this information, we segmented the apartment locations on a graph and identified a threshold below which a higher proportion of apartments were classified as 0 rather than 1. We incorporated this threshold as a binary variable in our model to capture the significance of the location feature.

Amenities Feature: We conducted an analysis of the amenities provided by each apartment. We identified specific amenities that exhibited a high correlation with the target variable. For such amenities, we created binary variables indicating their presence or absence. This helped us capture the influence of amenities on the classification of apartments as expensive or not.

### Imbalanced Dataset
We encountered a significant class imbalance in our dataset, with approximately four times as many apartments classified as 1 compared to apartments classified as 0. Initially, our model struggled to predict 0s accurately while performing well for 1s. To address this issue, we employed the Synthetic Minority Over-sampling Technique (SMOTE) library. By generating synthetic observations for the minority class (0), we balanced the dataset and significantly improved our model's performance.

### Hyperparameter Experiment
We conducted an extensive experiment to optimize the hyperparameters of our model. Specifically, we focused on the learning rate and the number of iterations. After testing various combinations, we found that the best results were obtained in the learning rate range of 1-1.2 and with a specific number of iterations.

Feel free to adjust the content and formatting based on your project's specific details and results.
