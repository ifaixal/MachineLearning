A type of gradient descent which is an optimization algorithm used for different models with convex function or non-convex function to find a minima or reduce the error cost function.

Batch gradient descent is effective in cases of Convex function, local minima is the global minima. With the assumption that the dataset is smaller.

In batch gradient descent for calculating the slope/gradient (error gradient) we utilize our whole dataset. 
Suppose you have 1,000 training examples.

1. Make predictions for **all 1,000 examples**.
2. Compute the loss over **all 1,000 examples**.
3. Compute the gradient of the loss with respect to the parameters using **all examples**.
4. Update the parameters **once**.

So there is **one parameter update per epoch**.