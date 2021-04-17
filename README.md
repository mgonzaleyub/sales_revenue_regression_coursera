# Sales Revenue Regression Analysis with scikit-learn
This project was done through Coursera Project Network [here](https://www.coursera.org/projects/scikit-learn-simple-linear-regression)

## Objective
We are trying to predict revenue sales values with respect to advertisement spends across multiple channles like radio, tv and newspaper.

The original dataset can be found here: http://www-bcf.usc.edu/~gareth/ISL/Advertising.csv

The algorithm used is *Linear Regression* available at _sklearn.linear_model_ package.

## Linear Regression Explanation
The lienar regression algorithm is based in the following formula:

![alt text](https://render.githubusercontent.com/render/math?math=f%28x%29%20%3D%20%5Cbeta_0%20%2B%20%5Csum_%7Bj%3D1%7D%5Ep%20X_j%20%5Cbeta_j&mode=inline "Linear regression formula")

where ![alt text](https://render.githubusercontent.com/render/math?math=X%5ET%20%3D%20%28X_1%2C%20X_2%2C...%2CX_p%29&mode=inline "Input features") vector are the input features
All betas are coefficients that must be adjusted, in other words: our model parameters; and Y vector will have the predicted values.

It's important to say that linear regression fits properly in data when they are supposed to be linear. Usually, a regularization term (L1, L2, ElasticNet) is also interesting
so as to avoid overfitting, but I'm not applying it this time.

## Feature Engineering
It's important to explore the data to gather even more information. In this project I am using:
- Distribution plots for each feature
- Pairplot for each pair of features related to the output.
- Correlation matrix: it's a squared matrix with a size of the number of features. Can take values between -1 and 1, where -1 tells that if one raises, the other loweres proportionally,
and viceversa.

We discover that TV feature is the most similar to a linear model, so we pick this feature to build the model.

## Evaluation Metrics
We need to evaluate the performance of the model, so we define some metrics that measure errors. An error can be defined as the difference between a predicted value and the real value.
* Mean Absolute Error (MAE) is the mean of the absolute value of the errors:

![alt text](https://render.githubusercontent.com/render/math?math=%5Cfrac%7B1%7D%7Bn%7D%20%5Csum_%7Bi%3D1%7D%5E%7Bn%7D%20%5Cleft%20%7Cy_i%20-%20%5Chat%7By%7D_i%20%5Cright%20%7C&mode=display "MAE formula")

* Mean Squared Error (MSE) is the mean of the squared errors:

![alt text](https://render.githubusercontent.com/render/math?math=%5Csqrt%7B%5Cfrac%7B1%7D%7Bn%7D%20%5Csum_%7Bi%3D1%7D%5E%7Bn%7D%20%28y_i%20-%20%5Chat%7By%7D_i%29%5E2%7D&mode=display "MSE formula")

* Root Mean Squared Error (RMSE) is the square root of the mean of the squared errors:

![alt text](https://render.githubusercontent.com/render/math?math=%5Csqrt%7B%5Cfrac%7B1%7D%7Bn%7D%20%5Csum_%7Bi%3D1%7D%5E%7Bn%7D%20%28y_i%20-%20%5Chat%7By%7D_i%29%5E2%7D&mode=display "RMSE formula")

## Certificate
![alt text](https://github.com/mgonzaleyub/sales_revenue_regression_coursera/blob/master/certificate.png "Completion certificate")
