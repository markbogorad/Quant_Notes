up:: [[Probability MOC]]
tags:: #Math
# Normal (Gaussian) Distribution
- The distribution is symmetric and describes how the values of a random variable are distributed, with most of the values clustering around the mean.
### Key Characteristics:
- **Mean $( \mu )$**: The mean $( \mu )$ represents the center of the distribution. It is the point at which the distribution is centered, and it is also the peak of the bell curve.
- **Standard Deviation $( \sigma )$**: The standard deviation $( \sigma )$ measures the spread or dispersion of the distribution. A smaller $( \sigma )$ results in a narrower and taller distribution, while a larger $( \sigma )$ results in a wider and flatter distribution.
- **Support**: The random variable \( X \) can take any real value, i.e., $( X \in (-\infty, \infty) )$.

### Probability Density Function (PDF):
The [[Probability Density Function (PDF)]] of a Normal distribution is given by:
$$f_X(x) = \frac{1}{\sigma \sqrt{2\pi}} \exp\left(-\frac{(x - \mu)^2}{2\sigma^2}\right), \quad x \in (-\infty, \infty)$$
### Notation:
A random variable $( X )$ that follows a Normal distribution with mean $( \mu )$ and standard deviation $( \sigma )$ is denoted as:
$$X \sim \mathcal{N}(\mu, \sigma^2)$$
### Cumulative Distribution Function (CDF):
The CDF of the Normal distribution, which gives the probability that the random variable \( X \) is less than or equal to a certain value \( x \), is denoted by $( \Phi(x) )$ and is defined as:
$$\Phi(x) = P(X \leq x) = \int_{-\infty}^{x} \frac{1}{\sigma \sqrt{2\pi}} \exp\left(-\frac{(t - \mu)^2}{2\sigma^2}\right) dt$$

### Mean (Expected Value):
The mean of the Normal distribution is:
$$E[X] = \mu$$
### Variance:
The variance of the Normal distribution is the square of the standard deviation:
$$\text{Var}(X) = \sigma^2$$

### Standard Normal Distribution:
The **Standard Normal distribution** is a special case of the Normal distribution where the mean $( \mu = 0 )$ and the standard deviation $( \sigma = 1 )$. It is denoted as:
$$Z \sim \mathcal{N}(0, 1)$$
For the standard normal distribution, the PDF simplifies to:
$$f_Z(z) = \frac{1}{\sqrt{2\pi}} \exp\left(-\frac{z^2}{2}\right)$$
- [[Standardization]]
	- Transforming a random variable to follow the standard normal
### Key Properties:
- **Symmetry**: The normal distribution is perfectly symmetric around its mean \( \mu \).
- **68-95-99.7 Rule**: About 68% of the data falls within one standard deviation \( \sigma \) of the mean, 95% falls within two standard deviations, and 99.7% falls within three standard deviations.
- **Uniqueness**: The mean \( \mu \) and variance \( \sigma^2 \) uniquely determine a normal distribution.

### Example:
$\textbf{Example: Newborns}$

$\textbf{Assumption:}$
$X \sim \mathcal{N}(3400, 320^2)$

$\textbf{Question:}$
What is the probability that $X < 2500?$

$\textbf{Solution:}$
$P(X < 2500) = P\left(\frac{X - 3400}{320} < \frac{2500 - 3400}{320}\right)$
$P(X < 2500) = P\left(Z < -2.81\right)$
- **Just plug in the given mean and std**
	- **X is in the inequality**

## From Bayes
- P(Z<X)
	- Probability that its less than the z variable
		- Z variable sets a border for where we integrate (basically the range of the tail)
- When `(-)` then do `1 - (the value if it wasn't negative)`
	- Same goes for P(Z>X)
- P(Y<X<Z)
	- P(Z<X) - P(Z<Y)
