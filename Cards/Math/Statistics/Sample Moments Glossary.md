up:: [[Probability MOC]]
tags:: #Math
# Sample Moments Glossary
## Population vs Sample
- **Population:** complete set of all items observed
- **Sample:** a subset of the population taken for testing
## Moment
- A function that captures a characteristic of a sample (mean, std, variance, etc)
## Variates
### Quantitative
- Continuous
	- Any characteristics that change gradually (can be infinite)
- Discrete
	- The set of numbers is finite
### Qualitative
- Ordinal
	- Some sort of rank amongst items
- Nominal
	- Data obtained from categorial questions (yes or no questions)
		- No order amongst data
## Sample Mean
$$
\bar{x} = \frac{1}{n} \sum_{i=1}^n x_i
$$
where:
- N is the number of observations
- Xi is the i-th observation
- [[Expectation]] of the mean is $\mu$, this means its unbiased
## Sample standard deviation
- The average change (deviation) away from the mean (average)
$$
s = \sqrt{\frac{1}{n-1} \sum_{i=1}^n (x_i - \bar{x})^2}
$$
where:
- (xi-x) is the difference between the i-th observation and the sample mean
### Rescaled sample standard deviation
$$
\delta = s \sqrt{\frac{n}{n-1}}
$$
- S is sample standard deviation
- Used for skewness and kurtosis calculations
## Sample variance
- Just the standard deviation squared (no square root in formula)
	- Assess dispersion (like standard deviation)
$$
s^2 = \frac{1}{n-1} \sum_{i=1}^n (x_i - \bar{x})^2
$$
## Sample kurtosis
- Measures the fatness of the tails of the distribution
	- Essentially this is the probability of outliers
$$
K = \frac{1}{N} \sum_{i=1}^N \left( \frac{y_i - \bar{y}}{\hat{\sigma}} \right)^4
$$
where:
- yi -> each individual observation
- y bar -> mean of observations
- Sigma -> sample standard deviation
## Sample skewness
- Measures the asymmetry of the distribution
	- Negative skewness -> leftward asymmetry (longer tail)
	- Positive skew -> rightward asymmetry
$$ 
S = \frac{1}{N} \sum_{i=1}^N \left( \frac{y_i - \bar{y}}{\hat{\sigma}} \right)^3
$$




