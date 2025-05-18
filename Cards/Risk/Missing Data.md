up:: [[Risk Management MOC]]
tags:: #Finance 
# Missing Data
- Types of missing data
	- Missing completely at random (rare)
		- A certain value is missing has nothing to do with hypothetical value and with values of other variables
		- Data remains unbiased in theory
	- Missing at random
		- propensity for data point to be missing not related to missing data, but related to some of the observed data
		- Cant verify this statistically - use substantive reasonableness
		- Can be corrected by correlating missingness to something
		- EX: In a medical study, older patients are less likely to report income, but among those of the same age group, missingness is random
	- Missing not at random
		- missing value depends on the hypothetical value (intentionally missing ex: rich people don't like to reveal salaries)
		- missing value dependent on missing values themselves
		- creates a bias
		- Ex: Patients with **higher income** refuse to disclose their salary, making the missing values systematically different from observed values

| Type     | Missing Mechanism         | Can be Ignored?     | Best Approach                                               |
| -------- | ------------------------- | ------------------- | ----------------------------------------------------------- |
| **MCAR** | Completely random         | Yes, no bias        | Listwise deletion, mean imputation, EM, multiple imputation |
| **MAR**  | Depends on observed data  | No, but correctable | Multiple imputation, EM algorithm                           |
| **MNAR** | Depends on missing values | No, serious bias    | Domain-specific models, sensitivity analysis                |
## Approaches to Missing Data
- Prior or next day fill
	- Dampens volatility (smooths it) because same value appears twice instead of there being jumps
- Interpolation
- [[Brownian Bridge]]
- Regression based missing data fill
	- Missing time series is the y in linest
	- Run linest on the sample as if the missing stuff wasnt there
	- Run a sum of the betas times coefficients for each empty time slots
	- EM fill
		- finds [[Maximum Likelihood Estimator]] estimations of parameters in models where direct optimization is difficult due to missing or unobserved data
- Bootstrap data
	- Random drawing from a historical sample
	- A [[Monte-Carlo Simulation]] technique
	- You set up random samples and then derive a path by multiplying the random samples to replicate changes over time (like 1+r * 1+r ** 1+r)
- Delete the row