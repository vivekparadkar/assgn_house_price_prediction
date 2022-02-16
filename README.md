# Project Name
> House Price prediction for australian market.


## Table of Contents
- [Project Name](#project-name)
  - [Table of Contents](#table-of-contents)
  - [General Information](#general-information)
  - [Conclusions](#conclusions)
        - [Ridge Regression](#ridge-regression)
        - [Lasso Regression](#lasso-regression)
  - [Technologies Used](#technologies-used)
  - [Contact](#contact)


## General Information
A US-based housing company named Surprise Housing has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price. The has collected data from the sale of houses in Australia.

The company is looking at prospective properties to buy to enter the market. Requirement is to build a regression model using regularization in order to predict the actual value of the prospective properties and decide whether to invest or not.

Company wants to know:
- Variables which are significant in predicting the price of a house
- How well those variables describe the price of a house
- Determine the optimal value of lambda for ridge and lasso regression


## Conclusions
From the regression analysis, we can clearly see that both Ridge and lasso regression are able to predict on both train and test set with high score:

##### Ridge Regression
Lambda - 6
Train R2 Score - 0.8908122407337311
Test R2 Score  - 0.8542564795841887
RMSE           - 0.039341341670644

##### Lasso Regression
Lambda - alpha=0.0001
Train R2 Score - 0.898066998511091
Test R2 Score  - 0.8508815744913294
RMSE           - 0.0397942380553869

R2 Score is almost same for both Ridge and Lasso. Alpha for ridge is 6 and for Lasso it is 0.0001. 

In this case, Lasso regression will be preferred since it does feature selection also, that is the variables which don't add much value to prediction are pushed to 0. Whereas in Ridge, we still need some way for feature selection since it does not have built-in feature selection.

From Lasso regression result, we can see that following results have positive correlation to the target SalePrice:

GrLivArea 	0.272
RoofMatl_WdShngl 	0.186
OverallQual 	0.119
Neighborhood_NoRidge 	0.072
GarageCars 	0.061

Following variables have negative correlation:
KitchenQual_TA 	-0.033
BsmtQual_Gd 	-0.033

From Ridge regression result, we can see that following results have positive correlation to the target SalePrice:

OverallQual 	0.078
2ndFlrSF 	0.073
GrLivArea 	0.066
RoofMatl_WdShngl 	0.064
Neighborhood_NoRidge 	0.064

Following have negative correlation:

BsmtQual_Gd 	-0.037
KitchenQual_TA 	-0.035
BsmtQual_TA 	-0.032


## Technologies Used
- matplotlib                3.5.0 
- numpy                     1.21.5
- pandas                    1.3.5 
- scikit-learn              1.0.2 
- seaborn                   0.11.2


## Contact
Created by vivekparadkar - feel free to contact me!