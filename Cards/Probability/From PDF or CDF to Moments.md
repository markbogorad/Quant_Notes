up:: [[Probability MOC]]
tags:: #Math
# Going from a PDF/CDF to the moments
## From PDF
$$\mathbb{E}(X) = \int_{-\infty}^{\infty} x f_X(x) \, dx$$
$$\mathbb{E}(X) = \sum_x x P(X = x)$$
- Integrate X by the [[Probability Density Function (PDF)]]
- The idea is to weight each possible value x by the probability density $fX​(x)$ and integrate over all possible values of $X$.
	- Think of this as multiplying all possible values by the weighted probability, giving you the mean

## From CDF
$$\mathbb{E}(X) = \int_{-\infty}^{\infty} \left(1 - F_X(x)\right) \, dx$$
- Take the inverse of the [[Cumulative Distribution Function (CDF)]]
- 