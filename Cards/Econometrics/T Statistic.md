up:: [[Probability MOC]], [[Econometrics MOC]]
tags:: #Math
# T Statistic
 - Used to test whether a particular regression coefficient is significantly different from zero (comes from T test) and therefore *significant in the model or not*
$$ \begin{equation} t = \frac{\hat{\beta} - \beta_0}{SE(\hat{\beta})} \end{equation} $$
where: 
	- β hat is the estimated coefficient.
	- β0 is the value of the coefficient under the null hypothesis (you choose this value)
	- SE(β^) is the [[Standard Error]] of the beta of the estimated coefficient.
formula for B hat
$$ \hat{\beta} = \frac{\sum_{i=1}^N x_i y_i - N \bar{x} \bar{y}}{\sum_{i=1}^N x_i^2 - N \bar{x}^2} $$
- B hat --> also the slope of the regression line
- N -> number of observations
- X -> independent variable
- y -> dependent variable
- x and y bar --> average values of x and y respectively

- Positive beta --> positive relationship between x and y
- Negative beta --> negative relationship

## T test
- A test that determines whether there is a significant difference between 2 groups
	- Tests whether a regression coefficient is equal to 0
- **Null Hypothesis (H0​):** βi=0 (the independent variable xi​ has *no effect* on the dependent variable y) [[Hypothesis Testing]]
- **Alternative Hypothesis (Ha):** βi≠0 (the independent variable xi​ *has an effect* on the dependent variable y)
- Critical values come from the [[T Distribution]]
