up:: [[Linear Algebra MOC]]
tags:: #Math
# [[Covariance]] Manipulations
- **Variance of a scaled variable**
	- $\text{Var}(aX) = a^2 \text{Var}(X)$
	- **Logic:** Scaling a random variable by a constant $a$ scales the variance by $a^2$. This is because variance measures the spread of the variable, and scaling stretches or compresses this spread.
	
- **Covariance of a variable with itself**
	- $\text{Cov}(X, X) = \text{Var}(X)$
	- **Logic:** The covariance of a variable with itself is simply its variance, as it measures how much the variable varies with respect to itself.
	
- **Covariance of 2 scaled variables**
	- $\text{Cov}(3X, 4Y) = 12 \text{Cov}(X, Y)$
	- **Logic:** When scaling two variables by constants, the covariance is scaled by the product of these constants. Here, $3×4=12$.
	
- **Covariance of a variable with a constant**
	- $\text{Cov}(X, a) = 0$
	- **Logic:** The covariance between a random variable and a constant is zero because *a constant does not vary*, so there is no shared variability.
	
- **Covariance of two linear combinations of variables**
	- $\text{Cov}(3X + 4Y, 5X + 6Y) = 15 \text{Var}(X) + 24 \text{Var}(Y) + 38 \text{Cov}(X, Y)$
	- **Logic:** This uses the **bilinear property of covariance**. Each term in the expansion involves the product of coefficients and the covariance between the corresponding variables:
	
- **Ratio of covariance to variance (BETA)**
	- $\frac{\text{Cov}(X, Y)}{\text{Cov}(X, X)} = \beta$    and     $\beta = \frac{\text{corr}(X, Y) \cdot \sigma_X \sigma_Y}{\sigma_X^2} = \frac{\rho_{XY} \sigma_Y}{\sigma_X}$
	- **Logic:** This represents the slope coefficient in a simple linear regression of $Y$ on $X$, known as the beta coefficient. It shows the sensitivity of $Y$ to changes in $X$. [[CAPM]]
- Covariance of a sum of variables with another variable
	- $\text{Cov}\left(\sum X_i, Y\right) = \sum \text{Cov}(X_i, Y)$
	- **Logic:** The covariance of the sum of several variables with another variable is the sum of the covariances of each individual variable with that variable. This follows from the linearity property of covariance.