---
layout: archive
title:  "Kaggle competition: House price prediction"
date:   2021-10-04
categories: jekyll update
author_profile: true
comments: true
classes: wide
---

Keywords: python, PCA, decision trees, random forest, boosting

In this small machine learning project, by using dataset from [Kaggle](https://www.kaggle.com/c/house-prices-advanced-regression-techniques), I created a machine pipeline that can accurately predict the sale prices for houses. 

This dataset contains 1460 observations with 79 features. I did following operations:

- Check for missing values and discard columns that contain too much missing information
- Impute missing values in numerical column by using Iterative Imputer
- Convert categorical columns with Onehot Encoder
- Create pipeline to apply imputing, standard scaling and machine learning models
- Test with PCA and without PCA
- Choose best parameters for machine learning models
- Finally apply on the test dataset provided by Kaggle for submission


![house_price](/assets/images/house_price_prediction.png)

Boosting methods gave better results. Best model in terms of highest accuracy was Gradient Boosting and best model in terms of smallest log RMSE was XGBOOST. 

Code can be found in [Github](https://github.com/esinkarahan/ml_house_price_prediction). 

