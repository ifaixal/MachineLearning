A supervised machine learning algorithm used to predict continuous numerical values (salary, temperature or price) by modeling the relationship between a dependent target and one or more independent features.
$$
Y^" = mx + b 
$$
Line of best fit, the line that with every data points is perfectly or with minimal margin.
b = offset. The starting position of the line,
w = weight,
x1 = feature 1 and so on.

#### Perfect Environment for Linear Regression:
- **Linearity:** The relationship between the independent and dependent variables must be a straight line.
- **Independence:** The observations in your dataset must be independent of one another.
- **Homoscedasticity:** The residuals (the errors between actual and predicted values) must be consistent across all values.
- **No Multicollinearity:** Independent variables should not be highly correlated with each other.

#### Types of Linear Regression
1. **Simple Linear Regression:** Uses exactly one independent variable to predict the target (e.g., predicting a house price based _only_ on its square footage).
2. **[[Multiple Linear Regression]]:** Uses two or more independent variables to make a prediction (e.g., predicting house price based on square footage, location, and age of the house).

For the evaluation of Linear Regression or regression models we have metrics. [[Regression Mertics]]
