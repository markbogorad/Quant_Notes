up:: [[Supervised Learning MOC]]
tags:: #Machine_Learning
# Linear Regression
- Most commonly used model in finance today
- A [[Supervised Learning]] [[Regression]] technique
- Linear means that the model outputs always depend on the sum of the inputs and the parameters.
	- Does not necessarily need to be a straight line, for example [[Logistic Regression]] is linear
## Univariate Regression
- Simply training the model to do Y as a function of X
## Least Squares Regression
- The goal of this is to minimize a cost function
$$J\left(\theta_{0}, \theta_{1}\right)=\frac{1}{2 m} \sum_{i=1}^{m}\left(h_{\theta}\left(x^{(i)}\right)-y^{(i)}\right)^{2}$$
- and we want to minimize
	- $\operatorname{minimize}_{\theta_{0}, \theta_{1}} J\left(\theta_{0}, \theta_{1}\right)$
### Minimize it with [[Gradient Descent]]
- 
