up:: [[Supervised Learning MOC]]
tags:: #Machine_Learning
# Logistic Regression
- Uses the sigmoid function
$$f(x) = \frac{L}{1+e^{-k(x-x_0)}}$$
- Data is squished into this function
	- $X_0$ is the midpoint of the sigmoid
	- $L$ is the maximum of the curve
	- $k$ is the logistic growth rate (steepness)
- Actually a [[Classification]] model (not regression)
	- Uses [[Maximum Likelihood Estimator]]
	- Has trouble capturing non-linear effects
	- Binary encoding --> useful for modeling probability
	- Sigmoid function --> boundary is L and it is divided by steepness (k)
		- Linear regression is embedded into loss function (uses linear input)
	- Uses logistic loss function --> loss function draws the sigmoid function (vs least squares drawing a straight line)
	$$  \mathcal{L} (y, f(x)) = -\underbrace{f_{y}(x)}_\text{score for true label} + \underbrace{\log \sum_{v=1}^{V} \exp (f_v(x))}_\text{soft-maximum score}$$
## Relationship to Odds Ratio and Probability
- If you express a probability as a function of the logistic, you get $ln\frac{p}{1-p}$ where $\frac{p}{1-p}$ is actually the **odds ratio**, i.e. probability of a win divided by probability of a loss
	- Natural log of odds ratio is **logit**
## Logit Under the Hood
$$p = \frac{1}{1 + e^{-\left(\beta_0 + \beta_1 X_1 + \cdots + \beta_k X_k\right)}}$$
- You essentially have a [[Regression]] in the denominator, where you evaluate the probability of being in group 1 (from numerator) as an exponential fraction of regressors
## Cost Function: Cross-Entropy
- This is a negated [[Log Likelihood]] function, negated so that we can minimize instead of maximize
- Evaluated using [[Classification Accuracy]]
## Why Use Logistic instead of [[Linear Regression]]
- Because you want to set a floor and ceiling -> like 0 and 1 for probability
- ![[Pasted image 20240829200304.png]]
- 