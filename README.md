# Building_Multiple_Linear_Regression_Model
> Note: The Dataset used here was got from SuperDataScience Training on Machine Learning.
> The First Seven records of the Sample Dataset is displaced below for insight into the data

## The Dataset: It contains 50 Startups, displaying their expenditure in different areas as seen in the table.
|R&D Spend|	Administration|	Marketing Spend|	State	|Profit|
|----------|---------------|----------------|-------|-------|
|165349.2|	136897.8|	471784.1|	New York|	192261.83|
|162597.7	|151377.59	|443898.53	|California	|191792.06|
|153441.51|	101145.55|	407934.54|	Florida|	191050.39|
|144372.41	|118671.85	|383199.62	|New York	|182901.99|
|142107.34|	91391.77|	366168.42|	Florida|	166187.94|
|131876.9	|99814.71	|362861.36	|New York	|156991.12|

## Definition: 
> Multiple linear regression (MLR) is a statistical method used to model the relationship between a dependent variable (the outcome you want to predict) and two or more independent variables (predictors or features). It extends simple linear regression, which uses only one independent variable, to scenarios where multiple variables influence the outcome.

## TheTask
> The task is to make a prediction for investor to know which company to invest in. The profit will then be the outcome of the model. Other columns besides profit are the independent variable.
> Note: The investor is not necessarily looking at high profit, he is also interested in if spending in Research or marketing yield better

## Equation for multiple linear regression (similar to simple LR)
$Y=β0 +β1X1 +β2X2 +⋯+βnXn$

Where:
> + Y: Dependent variable (target or outcome).
> + β0 : Intercept  (value of 𝑌 when all 𝑋𝑖 are 0).
> + β1 ,β2 ,…,βn : slope Coefficients representing the change in 𝑌
> + X1 ,X2 ,…,Xn Independent variables (predictors or features).

## Assumptions of Linear Regression
​
​
  
