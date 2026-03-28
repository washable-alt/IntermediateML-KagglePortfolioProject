# Intermediate ML Kaggle Portfolio Project

## Competition
[House Prices: Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/overview)

In this competition, a **lower score indicates better model performance**.

## Baseline
- Sample submission score: **0.40613**

## Models Tested

### Principal Component Analysis (PCA)
PCA is an **unsupervised dimensionality reduction technique** used to reduce the number of features before modeling.

### 1. Linear Regression
- Initial linear regression produced some **negative predictions**, which are not suitable for house prices.
- I then used **GammaRegressor**, which avoids negative outputs and predicts quickly.
- Score: **0.38457**

### 2. Random Forest Regressor with PCA
- Applied PCA before fitting a **Random Forest Regressor**.
- Score: **0.41415**

### 3. SGD Regressor with PCA
- Applied PCA before fitting a **Stochastic Gradient Descent (SGD) Regressor**.
- Score: **3.60018**
- This result was **not optimal**.

### 4. XGBoost Regressor without PCA
- Used **XGBRegressor** directly on the processed dataset without PCA.
- Score: **0.19093**

### 5. XGBoost Regressor with PCA
- Applied PCA before fitting **XGBRegressor**.
- Score: **0.48306**

## Summary
Among all the models tested, **XGBoost without PCA** achieved the best result with a score of **0.19093**, significantly outperforming the baseline and the other approaches.

## Key Takeaway
For this dataset, **PCA did not improve performance** for tree-based models such as Random Forest and XGBoost. The best performance came from **XGBoost without PCA**.
