up:: [[Probability MOC]]
tags:: #Math
# Covariance
- A measure of **linear dependance** between 2 [[Random Variables]], (see [[Independence]])
	- How much the two variables change together (are linearly related)
- The number derived from covariance is not a direct change
	- Rather, it measures the degree of joint variability
		- So 1 is strongly positively covariant, -1 is strongly negatively covariant
- Covariance of something with itself = [[Variance]]
- [[Correlation vs Covariance]]
- If X and Y are [[Independence]], then covariance = 0
	- Opposite is NOT true
## Mathematically
$$\text{Cov}(X, Y) = E[(X - E[X])(Y - E[Y])]$$
$$\text{Cov}(X, Y) = E[XY] - E[X]E[Y]$$
- Expectation of X - its own expectation $\times$ Y - its own expectation
	- [[Expectation]]







## Example (hard question from Bayes stats class)
### Problem Overview:
- **Given:**
  - Random variable $( X \sim U(-2, 2) )$ (Uniform distribution over $([-2, 2]))$.
  - Dependent variable $( Y = X^2 )$, which is a non-linear function of $( X )$.
  
- **Objective:**
  - Show that the covariance between $( X )$ and $( Y )$ is zero: $( \text{Cov}(X, Y) = 0 )$.
  - This demonstrates that $( X )$ and $( Y )$ are non-linearly dependent but linearly independent.
### Steps to Solve:
1. **Covariance Formula:**
   $\text{Cov}(X, Y) = E[XY] - E[X]E[Y]$

2. **Substitute $( Y = X^2 )$ into the Covariance Formula:**
   $\text{Cov}(X, Y) = \text{Cov}(X, X^2) = E[X \cdot X^2] - E[X]E[X^2]$
	 $\text{Cov}(X, Y) = E[X^3] - E[X]E[X^2]$

3. **Calculate the Expectations $( E[X^3] ), ( E[X] )$, and $( E[X^2] )$:**

   - **Probability Density Function (PDF):**
     $f_X(x) = \frac{1}{4} \quad \text{for } x \in [-2, 2]$

   - **Compute $( E[X] )$:**
     $E[X] = \int_{-2}^{2} x \cdot f_X(x) \, dx = \int_{-2}^{2} \frac{x}{4} \, dx = 0 \quad (\text{due to symmetry})$

   - **Compute $( E[X^2] )$:**
     $E[X^2] = \int_{-2}^{2} x^2 \cdot f_X(x) \, dx = \int_{-2}^{2} \frac{x^2}{4} \, dx$
     $E[X^2] = \frac{1}{4} \left[ \frac{x^3}{3} \right]_{-2}^{2} = \frac{16}{12} = \frac{4}{3}$

   - **Compute $( E[X^3] )$:**
     $E[X^3] = \int_{-2}^{2} x^3 \cdot f_X(x) \, dx = \int_{-2}^{2} \frac{x^3}{4} \, dx = 0 \quad (\text{due to symmetry})$

4. **Substitute Back into the Covariance Formula:**
   $\text{Cov}(X, Y) = 0 - 0 \cdot \frac{4}{3} = 0$
### Conclusion:
- The covariance $( \text{Cov}(X, Y) )$ is zero.
- **Key Insight**: $( X )$ and $( Y = X^2 )$ are non-linearly dependent but linearly independent.
- **Takeaway**: Covariance only measures linear dependence, not non-linear relationships.


## Change of Unit Formula
- How rescaled covariance relates to OG covariance
- It shows that scaling affects covariance directly by the scaling factors, while shifting (adding constants) does not affect covariance. 
- This result is often used in statistical analysis, especially when standardizing variables or when transforming data for analysis.
$$\text{Cov}(rX + s, tY + u) = E[(rX + s)(tY + u)] - E[rX + s]E[tY + u]$$
Expand product
$$E[(rX + s)(tY + u)] = E[rtXY + ruX + stY + su]$$
Subtract the product
$$E[rX + s]E[tY + u] = (rE[X] + s)(tE[Y] + u)$$
Combine and simplify
$$\text{Cov}(rX + s, tY + u) = rtE[XY] + ruE[X] + stE[Y] + su - \left(rtE[X]E[Y] + ruE[X] + stE[Y] + su\right)$$
**Final formula**
$$\text{Cov}(rX + s, tY + u) = rt \cdot \text{Cov}(X, Y)$$
