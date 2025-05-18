up:: [[Probability MOC]]
tags:: #Math
# Bivariate Normal Distribution
- An extension of the [[Normal Distribution]] for two dimensions 
	- Bell shape in 2 dimensions
- Two random variables X and Y are said to have a **bivariate normal distribution** if every linear combination of them is normally distributed. 
- The bivariate normal distribution is fully characterized by five parameters: 
	- the means $μX$​ and $μY$​, the variances $σX^2$​ and $σY^2$​, and the covariance $Cov(X,Y)$.
## PDF
$$f_{X,Y}(x,y) = \frac{1}{2\pi \sigma_X \sigma_Y \sqrt{1-\rho^2}} \exp\left(-\frac{1}{2(1-\rho^2)} \left[\frac{(x-\mu_X)^2}{\sigma_X^2} + \frac{(y-\mu_Y)^2}{\sigma_Y^2} - \frac{2\rho(x-\mu_X)(y-\mu_Y)}{\sigma_X \sigma_Y}\right]\right)$$



![[Pasted image 20240828183750.png]]
