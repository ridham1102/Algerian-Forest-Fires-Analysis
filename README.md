# Algerian Forest Fires Analysis

This repository presents a comprehensive study of the Algerian Forest Fires dataset, with a focus on predicting the Fire Weather Index (FWI). The analysis explores data ingestion, preprocessing techniques, feature selection, and the application of both traditional and regularized linear regression models.

## Project Objective

The principal aim of this work is to develop reliable regression models that can estimate the Fire Weather Index (FWI) using meteorological and environmental factors. A comparative assessment is conducted to understand the effects of multicollinearity and the benefits of regularization methods in improving predictive accuracy.

## Dataset Description

The dataset encompasses observations from two distinct regions in Algeria, including measurements of temperature, relative humidity, wind speed, rainfall, and other indices related to fire weather conditions. The target variable, FWI, quantifies the potential severity of forest fires.

## Analysis Workflow

### Data Acquisition and Exploration

The raw data is loaded and subject to initial inspection to verify structure, data types, and completeness. Descriptive statistics and visualizations are generated to identify patterns, outliers, and missing values.

### Data Cleaning and Preparation

Column names are standardized by removing leading or trailing whitespace. Irrelevant temporal attributes, such as day, month, and year, are dropped. Categorical fields, notably the fire classification label, are encoded into numerical representations to facilitate model training.

### Feature Selection

A correlation matrix is computed to pinpoint highly correlated predictors. Variables exhibiting excessive multicollinearity are removed to enhance model generalization and interpretability.

### Data Scaling

Numerical features are scaled using a standardization technique to ensure that all predictors share a common scale, which is particularly critical for models incorporating penalty terms.

## Modeling and Evaluation

### Linear Regression

An ordinary least squares (OLS) model is trained and evaluated using statistical metrics such as R², Mean Absolute Error (MAE), Mean Squared Error (MSE), and Root Mean Squared Error (RMSE). A detailed summary from the statsmodels library provides insight into coefficient significance and model assumptions.

### Regularized Regression

To counteract overfitting and multicollinearity, Lasso (L1), Ridge (L2), and Elastic Net (combined L1 and L2) regressions are implemented. Each model is assessed on the same evaluation metrics to compare performance and determine the effect of varying penalty strengths.

## Web Application

In addition to the analysis, a web application was developed using Flask. This application allows users to input relevant environmental parameters and receive a predicted Fire Weather Index (FWI) value based on the trained regression model. The application provides a simple and accessible interface for real-time predictions.


## Results and Conclusions

The findings demonstrate the trade-offs between bias and variance when employing regularization. While the OLS model offers an interpretable baseline, Lasso can eliminate irrelevant features and Ridge mitigates coefficient inflation. Elastic Net, as a hybrid approach, balances feature selection with coefficient shrinkage.

## Usage

1. Clone this repository.
2. Install required dependencies listed in `requirements.txt`.
3. Execute the Jupyter notebook `Algerian_Forest_Fires_Analysis.ipynb` to reproduce data processing steps and model training.
4. To run the web application, navigate to the Flask app directory and execute the `app.py` file.


