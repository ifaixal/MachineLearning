The bias-variance tradeoff is the balancing act between a model being too simple (high bias, leading to underfitting) and too complex (high variance, leading to overfitting).

**Bias:**
The inability of a machine learning model/algorithm to capture the true relationship in the training data is bias. The algorithm/model is not able to capture the underlying patterns in the training data. 
High bias often leads to Under-fitting.
Under-fitting phenomenon is when a machine learning algorithm has not been provided sufficient data or either the model is too simple to capture the underlying patterns of the dataset.

**Variance:**
The error caused by the model being too sensitive to the training data. High variance reflects overfitting, a phenomenon where the the model perform great on training data but when revealed to the unseen data it hallucinates or produce bad results.

Since the underlying function that generates the dataset is unknown we cannot directly utilize bias and variance instead we opt for other approaches for instance,
1. Train vs Validation performance:
	We measure the model performance on training data label after training and on testing data as well and compare the results if they are high in terms of error it reflects that our model is overfitting (rote learning).
2. Cross-Validation
3. Learning Curve
4. Error Metrics
	1. Classification: Accuracy, Precision, Recall, F1-Score, Log Score etc.
	2. [[Regression Mertics]]: MAE, MSE, RMSE, R<sup>2</sup> Score etc.