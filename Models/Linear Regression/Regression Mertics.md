For the evaluation of regression models we have metrics. These metrics help in the evaluation of the model performance. MAE, MSE, RMSE

**Mean Absolute Error:**
	It measures the average magnitude of errors between predicted and actual values, calculated by taking the sum of the absolute differences over the total dataset. A lower MAE indicates a more accurate model. $$MAE = \frac{1}{n}\sum_{i=1}^n|y_i - y_i^"|$$
	Where:
		n is the total number of observations.
		y<sub>i</sub> is the actual true value
		y<sub>i</sub><sup>'</sup> is the predicted value
		| y<sub>i</sub> - y<sub>i</sub><sup>'</sup> | represents the absolute difference/error.
	**Key Characteristics:**
		**Interpretability:** Because the error is calculated in the same units as the target variable, it is straightforward to understand. For example, in predicting house prices, an MAE of \\$5,000 means the model's predictions are off by an average of$5,000.
		**Robustness to Outliers:** Unlike Mean Squared Error (MSE), which squares the errors and thus heavily penalizes large deviations, MAE treats all errors equally. This makes it less sensitive to extreme outliers in your dataset.
	Our objective is to minimize the error as much as possible.
	The graph of modulus function is not differentiable at zero. A biggest drawback of Mean absolute value metric. Optimization technique such as gradient descent is the most difficult in such scenarios.

---
**Mean Squared Error:**
	Measures the average squared difference between estimated values and the actual true value. It is widely used in statistics and machine learning to evaluate how close a predictive model is to actual data. Lower values indicate better accuracy.$$MAE = \frac{1}{n}\sum_{i=1}^n(|y_i - y_i^"|)^2$$
	Where:
	n is total number of observation
	y<sub>i</sub> the actual value
	y<sub>i</sub><sup>'</sup> is the predicted value
	**Why Square the Errors?**
	Squaring the differences between actual and predicted values achieves two important things:
	1. **Prevents Cancellation:** Positive and negative errors are prevented from canceling each other out (e.g., a prediction that is 5 too high and one that is 5 too low will both result in a squared error of 25 rather than a net error of 0).
	2. **Heavy Penalization:** Because the errors are squared, large errors are penalized much more heavily than small errors, making the metric highly sensitive to outliers.
	
---
**Root Mean Squared Error:** (Output is in the similar metric as target variable)
	Because MSE squares the error terms, the final number is also in squared units rather than the original data's units. To get an error value that is easier to interpret in the original context, analysts often use the Root Mean Squared Error (RMSE), which is simply the square root of the MSE. $$RMSE = \sqrt{MSE}$$
	**Limitations and Applications**
	While its heavy penalty on large misses is great for optimizing models during training (such as with gradient descent), it can overemphasize extreme outliers. In cases where you want errors to be weighted linearly, Mean Absolute Error (MAE) is often used instead. MSE is prominently utilized in regression analysis, machine learning loss functions, image processing, and financial modeling

**R2 Score (Coefficient of Determination / Goodness of Fit):**
	The effectiveness of Linear regression (Model) in comparison to Mean of the actual dataset.
	A statistical metric that measures how well a regression model's predictions approximate real data. It ranges from 0 to 1, representing the proportion of variance in the dependent variable that is predictable from the independent variables.
	$$R^2 = 1 - \frac{SS_{res}}{SS_{tot}}$$
	Where: 
	SS<sub>res</sub> is the sum of squares of the residual errors.
	SS<sub>tot</sub> it the total sum of squares.
	**Quick Interpretation Guide:**
	- **1.0 (100%):** A perfect fit. The model explains all the variance in the target data.
	- **0.0 (0%):** The model performs no better than a baseline flat line predicting the average.
	- **<0.0 (Negative):** The model fits the data worse than simply guessing the mean, usually indicating a severe model error.
	The more we tend towards 1 the more effectiveness of the model is.
