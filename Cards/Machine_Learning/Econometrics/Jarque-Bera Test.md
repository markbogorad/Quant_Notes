up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# JB Test
- Tests whether or not a sample comes from a [[Normal Distribution]]
- Null: The sample data comes from a normal distribution.
- Alternative: The sample data does not come from a normal distribution.

## Test Statistic
$$ \text{JB} = \frac{n}{6} \left( S^2 + \frac{(K-3)^2}{4} \right) $$
- Test stat follows a [[Chi-squared Distribution]] with 2 degrees of freedom
- N: num of observations
- S: skewness
- K: kurtosis [[Sample Moments Glossary]]