up:: [[Econometrics MOC]]
tags:: #Math
# Heteroskedasticity
- **Homoskedasticity** (what we want): when errors are constant and spread of residuals does not depend on the independent variable (constant variance)
	- A key GM assumption of the [[OLS Estimator]]
- **Heteroskedasticity:** each individual will have a different shock and depends on the value of the independent variable (non constant variance)
![[0*jQ7I-M3BhknLRMXw.jpg]]
## Why it happens
- **Model Misspecification**: Incorrect functional form or omission of relevant variables.
- **Presence of Outliers**: Extreme values can increase variability.
- **Non-constant Variance**: The variance of the error terms naturally changes with the level of the independent variable(s).
- **Subpopulation Differences**: Different groups within the data may have different levels of variability.
## Remedies
- Transformations to variables: Dlog
- [[Huber-White Test]] correction and [[GARCH Correction]]
## Tests
 - [[White Test]]
	- [[Huber-White Test]]
- [[ARCH Test]]
	- [[GARCH Correction]]