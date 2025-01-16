up:: [[Linear Algebra MOC]], [[Unsupervised Learning]]
tags:: #Math #Machine_Learning 
# Principle Component Analysis (PCA)
## ML Theory
- Used when features are suspected to be linearly seperable
## Mathematics
- Simplifies complex datasets
- Goal: reduce as much dimensionality while maintaining variability of data
	- Transforms the original variables into uncorrelated variables called principle components, which are linear combinations of original variables
		- These components are [[Orthogonal Matrices]] (uncorrelated)
- [[Eigenvalues]] explain the proportion of the variance of each component
- [[Eigenvectors]] provide the direction of the components

![[Pasted image 20240704143852.png]]

### Example

Consider a dataset with daily returns of 100 stocks. Analyzing all 100 variables can be cumbersome. PCA can reduce these 100 variables to a smaller number of principal components (say, 5 or 10) that capture most of the variance in the returns. These components might represent underlying factors such as market sentiment, sector performance, or macroeconomic conditions.

- **Step-by-Step Process**:
    - **Compute the Covariance Matrix**: Calculate the covariance matrix of the stock returns.
    - **Eigenvalue Decomposition**: Perform eigenvalue decomposition on the covariance matrix to find the eigenvalues and eigenvectors.
    - **Select Principal Components**: Choose the principal components based on the eigenvalues (e.g., select components that explain 90% of the total variance).
    - **Transform Data**: Project the original data onto the selected principal components to obtain a reduced-dimension dataset.