up:: [[Probability MOC]]
tags:: #Math 
# PDF to CDF
$$F(x) = P(X \leq x) = \int_{-\infty}^{x} f(t) \, dt$$
- To go from the [[Probability Density Function (PDF)]] to the  [[Cumulative Distribution Function (CDF)]]
	- Logic:
		- The CDF represents the cumulative probability that X takes on a value less than or equal to x
		- To derive a CDF from the PDF, you integrate your PDF from $-\infty$ to x
			- Gives you cumulative probability up to x
## Example: normal dist
Let’s go through this with an example where $X∼N(0,1)$, the standard normal distribution.
1. **PDF**: The PDF for a standard normal variable $X$ is:
	- $f(x) = \frac{1}{\sqrt{2 \pi}} e^{-\frac{x^2}{2}}$
2. **Find the CDF**: integrate from $-\infty$ to x
	- $F(x) = \int_{-\infty}^{x} \frac{1}{\sqrt{2 \pi}} e^{-\frac{t^2}{2}} \, dt$
