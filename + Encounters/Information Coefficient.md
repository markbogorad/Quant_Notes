up:: [[Supervised Learning MOC]]
tags:: #Machine_Learning 
# Information Coefficient
- In finance, this is either Pearson or Spearman [[Correlation]]

## Pearson's Correlation
$$\rho(X, Y) = \frac{\text{Cov}(X, Y)}{\sigma_X \sigma_Y}$$
$$\rho(X, Y) = \frac{\sum_{i=1}^n (X_i - \bar{X})(Y_i - \bar{Y})}{\sqrt{\sum_{i=1}^n (X_i - \bar{X})^2} \sqrt{\sum_{i=1}^n (Y_i - \bar{Y})^2}}$$
- Only works on [[Continuous Functions]] and variables
- Only for linear relationships
- Sensitive to outliers
## Spearman's Correlation
$$\rho_s = 1 - \frac{6 \sum_{i=1}^n d_i^2}{n(n^2 - 1)}$$
- where
	- $( d_i )$ is the difference between the ranks of $( X_i )$ and $( Y_i )$.
	- $( n )$ is the number of data points.
- Adds a monotonic relationship to Pearsons correlation
	- Monotonic - as one variable increases, so does the other or vice versa
- Can be used for both linear and non-linear models