# Data Analytics Assignment 1
Documentation for House Price Regression Problem from preprocessing to model fitting [Kaggle Notebook Link](https://www.kaggle.com/namanjain412/notebook3e00b94058/edit) <br/>
[Github Link](https://github.com/namannjain/HousePricePrediction-ConvoAi-Data-Analytics)
<br/>
## Steps Followed:
1. Pre-Processing - a) Feature Selection, b) Median Imputation, c) Transformation and Scaling, d) PCA (Dimensionality Reduction) <br/>
2. Linear Regression <br/>
   a) Inbuilt Linear Regression (5 different algorithms) <br/>
   b) Inbuilt Ridge Regression ( Singular Value Decomposition, Eigenvalue Vectors) <br/>
3. Validation Accuracy

## Feature Selection
Initial Dataset had 79 features (excluding ID and output) and most were of object data-type.
I picked all features whose data-types matched the following four: <br/>
a) int64 <br/>
b) int32 <br/>
c) float64 <br/>
d) float32 <br/>
which resulted in 37 features. dataset shape - (1460,37) <br/>
 
## Imputation
Used median imputation to add median values to all the missing values in the dataframe <br/>

## Transformation and Scaling
1. Picked highly skewed features ,i.e, whose skewness>0.5 and applied log transformation (log_e(i+x)) on it. <br/>
2. Applied Standard Scaler for scaling the data so as to center the data around the mean to reduce bias towards any one feature. <br/>

## PCA (Dimensionality Reduction)
After the pre-processing steps, applied LinearRegression and got an R2score of 0.67 (close to 0.5). <br/>
Extracted major 5 Principal Components and used Ridge Regression on it to increase the r2 score.

## Linear Regression
Applied 2 inbuilt regression models - LinearRegression and Ridge and used the follwing 5 algorithms: <br/>
1) svd  2) eig  3) qr  4) svd-qr  5) svd-jacobi <br/>

## Validation Accuracy
![image](https://user-images.githubusercontent.com/70437311/156221461-3b57ba3c-b081-45db-b2d6-1e73e37e5dd4.png)
