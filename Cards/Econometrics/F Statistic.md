up:: [[Probability MOC]], [[Econometrics MOC]]
tags:: #Math
# F Statistic
- A test to see if the entire model is significant or not (all betas and intercept are different from 0 simultaneously). Basically a [[T Statistic]] test on ALL regressors at once
	- Tells you if the model is basically usable or not
$$ F = \frac{R^2 / (k - 1)}{(1 - R^2) / (T - k)} $$
where
- R^2: [[R Squared]]
- T: total observations
- K: number of parameters (regressors)

Alternatively:
$$F = \frac{N - k}{m} \left[ \frac{\text{RRSS} - \text{URSS}}{\text{URSS}} \right] \sim F_{m, N - K}$$
where
- m: number of hypothesis you are testing, or the amount of restrictions you have, or the difference in the number of parameters between RRSS and URSS
- URSS: unrestricted residual sum of squares (the model as is)
- RRSS: restricted residual sum of squares, this imposes the null hypothesis to be true
- Fm,N−K​: [[F Distribution]] with mm and N−KN−K degrees of freedom.