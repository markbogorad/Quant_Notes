up:: [[Quantitative Valuation MOC]]
tags:: #Finance  
# Control Variate
- Reducing variance of a variable $Y$ by leveraging the fact that we know the moments of $X$
	- Leverage a variable with a known expected value to reduce the variance of your estimate
- In a linear setting
	- $Y = bX$, where $b$ is the estimated coefficient from the regression
		- This will have an error term called **residual variance**, 
- **Mean response**
	- The expected average value of $Y$ for a given $X$
	- This is essentially saying, “Given $X=X_h$​, what do we expect $Y$ to be on average?”
	- The **variance of the mean response** is given by the equation, this is to compute standard error
	$$\text{Var}(X_h' b) = s^2 X_h' (X'X)^{-1} X_h$$
		- where:
		    - $s^2$ is the residual variance from the regression (a measure of how much the actual values of $Y$ vary from the predicted values).
		    - $X_h$​ is the specific value of $X$ we’re considering.
		    - $(X′X)^{−1}$ is a matrix that comes from the regression and helps account for how much information we have about the relationship between $X$ and $Y$.
		    $$\text{Reduction} = 1 - \frac{\text{Var}(X_h' b)}{\text{Var}(X_h b)} \text{- - -   OR - - - }\text{Reduction} = 1 - X_h' (X'X)^{-1} X_h$$
	- **Interpretation**: This variance tells us how much uncertainty we have in our estimate of $Y$ for a given $X=X_h$​. When $X$ is close to its mean value, the variance of the mean response is generally smaller, meaning our predictions are more precise. As $X$ moves away from its mean, this variance tends to increase, meaning our predictions for $Y$ become less certain.
	- By focusing on the variance of the mean response (which is generally lower than the overall variance of $Y$), we get a more precise prediction of $Y$. This reduced variance in our predictions translates to lower error in simulations or models, making our results more reliable.

residual variance - original variance = reduction in variance


## J
$$X_{CV} = X - \beta (Y - \mathbb{E}[Y])$$
$$\mathbb{E}[X_{CV}] = \mathbb{E}[X]$$
$$\text{Var}(X_{CV}) = \sigma_X^2 + \beta^2 \sigma_Y^2 - 2 \beta \sigma_{X,Y}$$
- Then solve for a $\beta$ that minimizes the variance
$$\beta^* = \frac{\sigma_{X,Y}}{\sigma_y^2}$$
- The greater the correlations between X and Y, the higher the variance reduction