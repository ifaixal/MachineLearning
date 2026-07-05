The phenomenon where the number of feature exceeds a threshold affecting the model performance thus increasing computation cost is curse of dimensionality.

Dimensionality can be considered as Features. Where features are number of column in a dataset.

Finding an optimal number of features is an objective of machine learning engineer. The optimal number of features are those feature which yield better results thus reducing the computation cost.

For instance, in an image model we encounter a 28x28 dimension image. 784px image now if we treat every pixel as an independent feature and in order to process 784 features it is computationally expensive, what we rather do is apply a set of algorithm that extracts the optimal number of pixels that can be processed for better results.

In higher dimension we encounter sparsity. This occurs in algorithms (such as recommendation engines) where most input features or data points are absent or unfilled.

The solution is dimensionality reduction.

#### Dimensionality Reduction
1. Feature Selection
	1. Forward Selection
	2. Backward Elimination
2. Feature Extraction
	1. [[Principle Component Analysis (PCA)]]
	2. Linear Discriminant Analysis (LDA)
	3. t-SNE and UMAP
	4. Auto-Encoders