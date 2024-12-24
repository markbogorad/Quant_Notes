up:: [[Supervised Learning MOC]]
tags:: #Machine_Learning
# Logistic Regression
- actually a classification model (not regression)
	- Has trouble capturing non-linear effects
	- Binary encoding --> useful for modeling probability
	- Sigmoid function --> boundary is L and it is divided by steepness (k)
		- Linear regression is embedded into loss function (uses linear input)
	- Uses logistic loss function --> loss function draws the sigmoid function (vs least squares drawing a straight line)
	$$  \mathcal{L} (y, f(x)) = -\underbrace{f_{y}(x)}_\text{score for true label} + \underbrace{\log \sum_{v=1}^{V} \exp (f_v(x))}_\text{soft-maximum score}$$
## Why Use Logistic instead of [[Linear Regression]]
- Because you want to set a floor and ceiling -> like 0 and 1 for probability
- ![[Pasted image 20240829200304.png]]
- 