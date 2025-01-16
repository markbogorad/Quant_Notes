up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# R Squared
- Goodness of fit measure, good for cross sectional data [[Time Series, Cross Sectional, Panel Data]]
- In sklearn [[Python MOC]], its automatically embedded in `score` in `(lr.score(X_test, y_test))`
	- Also in `metrics.r2_score`
## Problems with R Squared
- Highly dependent on range - MSE is the better loss function generally
	- [[MSE, RMSE, MAE, SMAPE]]
- Only reliable for linear modeling (no non linear modeling is valid r-squared)
	- Equation SST = SSR + SSE --> only holds if linear data
		- SST is sum of squares total
## Older Undergrad Notes
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
