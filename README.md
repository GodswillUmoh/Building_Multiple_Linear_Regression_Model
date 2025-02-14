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
   
   [See All Assumptions Here, Click to View](https://ibb.co/3Sxm9sG)

+ 4. Independence
  > Independence in statistics refers to a situation where two or more variables or events are not influenced by each other. If variables are independent, the occurrence or value of one variable does not affect the occurrence or value of another.
  > 
  > __Correlation vs. Independence:__ (of Observation, includes 'no autocorrelation'
  > While correlation measures the strength and direction of a linear relationship between two variables, independence implies no relationship of any kind. A correlation of 0 does not guarantee independence; the variables could be non-linearly related.
  > Typical Example for independence is the stock market

+ 5. Lack of multicollinearity (Predictors (independent variable) are not Correlated with each other; usually we will require the IV not to correlate with each other. If they are not correlated, then we can build a linear regression. If we go ahead to build, then the coefficient estimate will become unreliable). 

  > Lack of multicollinearity refers to a desirable condition in regression analysis where the independent variables (predictors) are not highly correlated with each other. When multicollinearity is minimal or absent, each independent variable contributes unique information to the model, enabling more reliable estimation of regression coefficients.
  > 
  > __What is Multicollinearity?__ 
Multicollinearity occurs when two or more independent variables in a regression model are highly correlated, meaning they share a significant amount of the same information. This can make it difficult to determine the individual effect of each variable on the dependent variable.
  >

+ 6. The Outlier Check (This an addition, not an assumption):
     
     [See Sample of Outliers in graph, click Here to view](https://ibb.co/8Ns0LpB)
     
  > An outlier check involves identifying and assessing data points that deviate significantly from the other observations in a dataset. Outliers can have a disproportionate impact on statistical models, influencing the results and potentially leading to inaccurate conclusions.
  > Why Check for Outliers? Distort Statistical Analysis: Outliers can skew means, variances, and other statistical measures.
  > __Methods to Identify Outliers:__
  > _Visual Inspection:_
  > + Box Plot: Displays the interquartile range (IQR), and points outside 1.5 × IQR are flagged as potential outliers (Identifying Outliers: Outliers are data points that fall outside the whisker boundaries. Any data point below the lower bound or above the upper bound is considered an outlier).
  > + Scatter Plot: Useful for bivariate data to spot outliers relative to other observations.
  >   
  >   __Three Main Analysis Carryout On Variables are:__
  >   + __Univariate Analysis__: Definition: Involves analyzing a single variable to understand its distribution, central tendency, and spread. Objective: Summarize and describe the data. Dataset: e.g Heights of students (5.1,5.7,6.0,5.5).
  >     
  >   +  __Bivariate Analysis__: Definition: Examines the relationship between two variables, often involving dependent and independent variables. Objective: Determine the association, correlation, or dependency between two variables. e.g Dataset: Relationship between hours studied (independent) and exam scores (dependent).
  >     
  >   +  __Multivariate Analysis__: Definition: Involves the analysis of three or more variables simultaneously to explore complex relationships. Objective: Understand the interactions and dependencies among multiple variables. Techniques: Multiple Regression: Model the relationship between one dependent and several independent variables.
  >     e.g Dataset: Analyze factors influencing house prices (e.g., size, location, and age of the house).

## Python Code for Multiple Linear Regression
+ [Click Here to view code for MLR](https://colab.research.google.com/drive/1r2h0lr7V37XiVTXk7GAs05-8OHr8G6tW)

##  Anscombe’s Quartet
+ [To see image, click to view](https://ibb.co/TMfb0jZV)




