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
The Anscombe's quartet that is dataset in four pattern showing the different ways variables relate. Linear regression is not applied in the ones that the graph do not show linearity.
> __Anscombe's quartet__ is a collection of four datasets, each consisting of 11 data points, designed to demonstrate the importance of visualizing data before analyzing it statistically. These datasets have nearly identical simple descriptive statistics (e.g., mean, variance, correlation, and regression line), but when visualized, they reveal very different patterns and relationships.

## [See Image of Anscombe Quartet Here:](https://ibb.co/jMTZYcY)

> __Key Statistics of Anscombe’s Quartet:__  For all four datasets, when graphed:
> + Dataset 1: A linear relationship fits well; the data aligns closely with the regression line.
> + Dataset 2: A clear non-linear relationship; a curve would better fit the data.
> + Dataset 3: An outlier skews the regression, although most points form a horizontal line.
> + Dataset 4: A vertical line, where all points except one have the same x-value, making the regression line misleading.
>
> Hence, Linear Regression is only fit in the Dataset 1 Scenario

## Importance of Anscombe’s Quartet
> The quartet highlights the risks of relying solely on numerical summaries without examining the data visually. Key lessons include:
> + Outliers matter: Outliers can strongly influence statistical summaries and regression models.
> + Patterns matter: Similar statistics can result from data with very different distributions and relationships.
> + Visualization is crucial: Always visualize your data to understand its true nature.

_In modern contexts, it also inspires similar examples like the Datasaurus Dozen, which shows datasets with identical statistics but wildly different shapes when visualized._
​
## Therefore, The Assumptions for Linear Regression
+ 1. Linearity: Linear Relationship Between Y and Each X 
+ 2. Homoscedasticity (Equal Variance)
  >Homoscedasticity refers to a key assumption in regression analysis and other statistical models. It means that the variance of the residuals (errors) is constant across all levels of the independent variable(s). In simpler terms, the spread of the errors is uniform, regardless of the value of the predictors.

  [View Homoscedasticity Diagram Here, Click to View](https://ibb.co/X5kJLZK)
  >  __Why is Homoscedasticity Important?__
  > + Assumption in Regression: Many statistical tests, including linear regression, assume homoscedasticity. Violating this assumption can lead to biased estimates of coefficients and unreliable hypothesis tests.
  > + Fair Predictions: Consistent error variance ensures that the model's predictions are equally reliable across all values of the independent variables.
  
+ 3. Multivariate normality (Normality of Error Distribution)
   > Multivariate normality is an extension of the concept of univariate normality to multiple variables. It describes a situation where a set of variables follows a multivariate normal distribution. This concept is critical in multivariate statistics, as many analyses (e.g., multivariate regression, MANOVA, and factor analysis) assume multivariate normality.

[See All Assumptions Here, Click to View](https://ibb.co/jHk30Ny)

+ 4. Independence
  > Independence in statistics refers to a situation where two or more variables or events are not influenced by each other. If variables are independent, the occurrence or value of one variable does not affect the occurrence or value of another.
  > 
  > __Correlation vs. Independence:__ (of Observation, includes 'no autocorrelation'
  > While correlation measures the strength and direction of a linear relationship between two variables, independence implies no relationship of any kind. A correlation of 0 does not guarantee independence; the variables could be non-linearly related.
  
