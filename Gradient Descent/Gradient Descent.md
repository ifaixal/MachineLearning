### Rule of thumb
If the optimization problem is **convex**, gradient-based optimization can find the global optimum. Most **classical machine learning** algorithms (linear models, logistic regression, SVMs, regularized regression) are convex, while most **deep learning** models are non-convex.

Gradient descent is a first-order iterative optimization algorithm for finding a local minimum of a differentiable function.
It is an optimization algorithm. Beside linear regression aggressively used in deep learning. 
The reason gradient descent is used in deep learning is, Since neural network contain millions of complex, non-linear parameters, a direct mathematical solution to find the absolute lowest error does not exist; gradient descent provide a scaleable, step-by-step approximation method to achieve this.
#### Intuition:
Linear regression can be derived using Open Least Square, and gradient descent can be used to derive the value of b. Since the loss function and b follows a parabolic relationship. As parabolic relationship is differentiable instead of OLS we prefer Gradient descent for the local minima. Due the reason that in higher dimensions setting the value to zero (for b) and finding the minima is problematic and hard to perform. 

**The Learning Rate:**
The size of the steps taken in gradient descent is controlled by a crucial hyperparameter called the **learning rate** (α).
- **Too small:** The steps will be tiny, requiring a massive amount of time and computations to reach the minimum.
- **Too large:** The step will be too big, potentially causing the model to overshoot the target, bounce around, or even diverge entirely.
For a deeper look into the mathematics and how step sizes dictate convergence:

**Variants of Gradient Descent**
Depending on the size of the dataset, there are three primary variants used in training:
1. **Batch Gradient Descent:** Computes the error for _each entire dataset_ and updates the model after evaluating all examples. It is stable but can be very slow for massive datasets.
2. **Stochastic Gradient Descent (SGD):** Computes the gradient and updates the model for _one training example at a time_. It is much faster and more erratic, which can help the model escape local minimums.
3. **Mini-Batch Gradient Descent:** The most commonly used approach. It splits the training data into small batches (e.g., 32, 64, or 128 samples) to update the model, combining the stability of batch gradient descent with the efficiency of SGD

**Analogy:**
Imagine you are at a mountain surrounded by fog and you want to reach the lowest point where's a food stall exist. Since, you are surrounded by fog and unable to know the direction. You take a small step and check which direction slope downwards the most.

Error
 ^
 |        ● Start
 |       /\
 |      /  \
 |     /    \
 |    /      \
 |   /        \____ Minimum error
 +-----------------------------> Parameters (weights)
$$
New weight=Old weight−learning rate×gradient
$$$$New Weight = Oldweight - α\frac{dL}{dw}$$
**One sentence to remember:**
> *Gradient = which way is uphill. Gradient descent = take small steps downhill until you reach the lowest point.*

**Working:**
- **Initialize Parameters**  
    The algorithm starts by assigning random or zero values to the model's weights (**w**) and biases (**b**).
- **Calculate the Loss**  
    The model makes a prediction using the current parameters, and a loss function measures how "wrong" the prediction is compared to the actual target data.
- **Compute the Gradient**  
    The algorithm calculates the partial derivative (gradient) of the loss function with respect to each individual parameter. The gradient represents the slope of the mathematical hill, pointing directly "uphill" toward higher error.
- **Update the Parameters**  
    To reduce the error, the algorithm subtracts a fraction of the gradient from the current parameter value. This moves the parameters "downhill".
- **Repeat Until Convergence**  
	Steps 2 through 4 are repeated for many iterations (epochs). The process stops when the gradient is close to zero, meaning the loss function has hit its minimum point (convergence).

1. You start at a **random location** on the mountain (random weights).
2. You measure your altitude. Suppose it's **1000 m** (high loss).
3. You feel the slope under your feet. You notice the ground slopes downward toward the east. That's the **gradient**telling you which way is uphill; you walk in the opposite direction.
4. You take a small step east.
5. Now you're at a new position. Your altitude is **990 m** (lower loss).
6. **You do not use the previous slope to decide the next step.** Instead, you **feel the slope again at your new location**, because the terrain has changed.

So every iteration is:

- Current weights → make prediction → compute loss → compute gradient **at those current weights** → update weights.

$$y=x^4-3x^3+2$$
==Gradient descent does _not_ guarantee finding the global minimum for arbitrary loss functions.==

**Types:**
[[Batch Gradient Descent]]
