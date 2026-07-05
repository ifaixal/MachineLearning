A Feature Extraction technique with an objective of reducing the dimensionality or eliminating curse of dimensionality. Reducing Feature

Principal Component Analysis (PCA) is ==a dimensionality reduction technique used to simplify large datasets while preserving their most important trends and patterns==. It transforms correlated variables into a smaller set of uncorrelated variables—called principal components—by finding the directions of maximum variance in the data.

Analogy is a photographer is in a football stadium that is in 3-Dimension, the photographer clicks a picture converting the environment to a 2-Dimension. i.e. Removing unnecessary information and keeping the true essence of the moment.

##### Benefits
1. **Feature** **extraction**
2. **Visualization**, Since it is easier for human organism to visualize up-to 2-Dimensions.
3. **Multicollinearity Handling:** It eliminates highly correlated variables by creating entirely new, independent composite variables

Number of Principle component <= Number of Features.

Why variance instead of mean absolute deviation ? Due to negative values since mean absolute deviation do not handle negative values effectively.

![[Pasted image 20260705121709.png]]
From the figure it is visible that upon projection of the spread of data points on x-axis it yield greater distance i.e. the innate nature is intact meanwhile on y-axis the distance is reduced hence the machine learning algorithms that deals with distance like KNN will be confused that such small distance yet so much differences. That is why we take the projection of the spread on axis that is the longest.

##### Covariance:
A statistical property used to find the relations among two variables. whether positive or negative or neutral.

#### How to use PCA:
1. Standardize the dataset. Using StandardScaler. For Mean-Centering.
2. Apply PCA from the Scikit Learn Library.

#### Finding optimum number of Principle components:

**Explained Variance and Explained Variance Ratio:** The **explained variance** tells us how much of the total variance in the data is captured by each principal component. The **explained variance ratio** is the proportion of the total variance explained by each individual component. This is used to _find optimal number of components in PCA_.

There are 2 methods to find optimal number of components:

(I) By plotting the cumulative explained variance, we can visualize how much total variance is retained as we add more components.
```
import numpy as np  
import matplotlib.pyplot as plt  
  
plt.plot(np.cumsum(pca.explained_variance_ratio_))  
plt.xlabel('Number of Principal Components')  
plt.ylabel('Cumulative Explained Variance')  
plt.show()
```

(II) Setting a specific threshold for the cumulative explained variance allows us to programmatically select the optimal number of components. For example, a common threshold is **90%**, meaning that we want to retain components that explain at least 90% of the variance.(We can use other threshold values too.)
```
import numpy as np  
threshold = 0.90 # For 90% explained variance  
cumulative_variance = np.cumsum(pca.explained_variance_ratio_)  
n_components = np.argmax(cumulative_variance >= threshold) + 1  
  
print(f"Number of components that explain {threshold*100}% variance: {n_components}")
```
#### When does PCA not Work?
- Pattern in higher dimension.
- ==when relationships are non-linear, features are completely uncorrelated, or separation depends on low-variance features rather than high-variance ones==.