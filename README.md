# House Price Prediction – Data Preprocessing Pipeline

## Project Overview

This project focuses on building a complete data preprocessing pipeline for a House Price Prediction dataset (House_Pricing.csv).
The goal is to clean, transform, and prepare the dataset for machine learning modeling by applying standard data preprocessing techniques such as handling missing values, encoding categorical variables, scaling features, and removing outliers.


## Dataset Description

The dataset contains various features related to house properties such as:

Number of bedrooms and bathrooms
Area measurements (square feet)
House condition and location-based attributes
Renovation details
Target variable: SalePrice

## Steps Performed
### 1. Dataset Loading & Exploration
Loaded the dataset using Pandas
Used .info() to check:
Data types
Missing values
Feature overview
Used .describe() to understand:
Statistical summary of numerical features
Distribution insights
### 2. Duplicate Removal
Checked for duplicate rows and removed them if present
Identified duplicate columns based on identical values and dropped them
### 3.  Missing Value Handling
Identified missing values in each column
Applied the following strategies:
Numerical columns → Mean / Median imputation (based on distribution)
Categorical columns → Mode imputation
Documented feature-wise handling strategy
### 4.  Feature Scaling
Identified numerical features excluding SalePrice
Applied scaling techniques:
StandardScaler / MinMaxScaler (based on feature distribution)
Ensured all numerical features are on a comparable scale
### 5.  Categorical Encoding
Identified categorical variables
Applied:
One-Hot Encoding for nominal features
Label Encoding for ordinal features (if applicable)
### 6. Outlier Detection & Removal
Used IQR (Interquartile Range) method
Detected outliers in numerical columns
Removed extreme values that could distort model performance
### 7. Train-Test Split
Defined SalePrice as the target variable
Split dataset into:
Training set: 80%

## Libraries Used
pandas

numpy

matplotlib / seaborn

scikit-learn
Testing set: 20%
Used train_test_split from sklearn
