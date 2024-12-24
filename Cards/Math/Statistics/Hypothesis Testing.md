up:: [[Probability MOC]]
tags:: #Math
# Hypothesis Testing
- Used to determine whether or not there is enough evidence in a sample of data to infer a **certain condition to be true for the entire population**
## How it works
1) State a null hypothesis and alternative hypothesis
	- **Null hypothesis:** what you aim to test against - this is the statement of no effect essentially
		- Wan't to reject this
	- **Alternative hypothesis:** the resulting belief if you reject the null hypothesis (what you want to prove)
2) Choose a significance level (α)
	- This level is the probability of rejecting the null hypothesis
	- Typically 5%
	- Equivalent to the risk of making a **type 1 error**
		- **Type I Error**: Rejecting the null hypothesis when it is actually true (**false negative**)
		- **Type II Error**: Not rejecting the null hypothesis when it is actually false (**false positive**)
		- **Power of a Test**: The probability that the test will correctly reject a false null hypothesis (1 - probability of Type II error).
3) Calculate test statistic
	- Matches whichever distribution you use
		- Z test stat -> [[Normal Distribution]]
		- T test stat -> [[T Distribution]]
		- Chi square test stat -> [[Chi-squared Distribution]]
		- F stat -> [[F Distribution]]
4) Determine the p-value
	- If the p value is less than or equal to the significance level α, you reject the null hypothesis.