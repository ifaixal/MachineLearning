$$Y^" = b + w_1x_1 + w_2x_2 + ... + w_nx_n$$
Multiple linear regression (MLR) is a statistical technique used to model the linear relationship between a ==single dependent variable and two or more independent (predictor) variables.== It calculates a ==line of best fit==, allowing analysts to predict outcomes and determine how much each independent variable influences the target.
**Core Assumptions:**
For an MLR model to be considered reliable, your data must meet the following criteria:
- **Linearity:** There must be a linear relationship between the dependent variable and the independent variables.
- **Homoscedasticity:** The variance of the error terms must remain constant across all levels of the independent variables.
- **Multivariate Normality:** The residuals (errors) of the model should be approximately normally distributed.
- **No Multicollinearity:** The independent variables should not be highly correlated with each other. When variables are heavily correlated, it skews the coefficients, making it difficult to figure out which variable is truly driving the prediction.

**Evaluation Metrics:**
To determine how well your MLR model fits the data, you will look at specific statistical indicators:
- **Multiple R-squared:** Represents the proportion of variance in the dependent variable that can be explained by the independent variables.
- **Adjusted R-squared:** A modified version of R-squared that penalizes you for adding variables that do not actually improve the model. It is highly recommended to use Adjusted R-squared in MLR.
- **P-values:** Help determine if a specific independent variable has a statistically significant relationship with the dependent variable.
