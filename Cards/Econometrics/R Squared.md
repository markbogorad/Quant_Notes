up:: [[Probability MOC]], [[Econometrics MOC]]
tags:: #Math
# R Squared
- It measures the proportion of the total variation in the dependent variable (output) that can be explained by the independent variables (inputs) in the model
- An indicator of in sample model performance (goodness of fit)
	- Ex: R squared of 67% --> 67% of variability in the data is explained by the model
- Standardized by the mean of observations (y bar), see formulas:
$$ R^2 = \frac{ESS}{TSS} = 1 - \frac{RSS}{TSS} $$
- TSS is total sum of squares (y is dependent variable and y bar is avg):
$$ \text{TSS} = \sum_{i}(y_i - \bar{y})^2 $$
- ESS is explained sum of squares (y hat is predicted value of dependent variable):
$$ \text{ESS} = \sum_{i}(\hat{y_i} - \bar{y})^2 $$
- RSS is residual sum of squares (u is the residuals or errors):
$$ \text{RSS} = \sum_{i}\hat{u_i}^2 = \sum_{i}(y_i - \hat{y_i})^2 $$
- And:
$$ \text{TSS} = \text{ESS} + \text{RSS} $$
