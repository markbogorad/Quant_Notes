up:: [[Probability MOC]]
tags:: #Math 
# Standardization (Z-Score)
- Standardization is the process of transforming a random variable $X $with any mean $μ$ and standard deviation $σ$ into a new random variable $Z$ that has **a mean of 0 and a standard deviation of 1**. This new variable Z follows the standard [[Normal Distribution]]
### Why Standardize?
- **Comparison**: Standardization allows us to compare different distributions by putting them on the same scale.
- **Simplification**: It simplifies calculations, especially when using statistical tables like the Z-table, which is based on the standard normal distribution.
- **Normalization**: Standardizing data can be a step in data preprocessing for machine learning models to ensure that all features contribute equally to the model.
### How to Standardize:
To standardize a random variable $( X )$, you subtract the mean $( \mu )$ and divide by the standard deviation $( \sigma )$:
$$Z = \frac{X - \mu}{\sigma}$$
Where:
- $( Z )$ is the standardized variable, which follows the standard normal distribution $( Z \sim \mathcal{N}(0, 1) )$.
- $( X )$ is the original variable with mean $( \mu )$ and standard deviation $( \sigma )$.
- $( \mu )$ is the mean of $( X )$.
- $( \sigma )$ is the standard deviation of $( X )$.

### Example:
Suppose \( X \) represents the scores on a test that are normally distributed **with a mean of 75** and a **standard deviation of 10**. To find the standardized score (Z-score) for a test score of 85:

$$Z = \frac{85 - 75}{10} = \frac{10}{10} = 1$$

This means a score of 85 is 1 standard deviation above the mean.

### Interpretation of Z-Score:
- **Z = 0**: The value \( X = \mu \) is exactly at the mean.
- **Z > 0**: The value \( X \) is above the mean.
- **Z < 0**: The value \( X \) is below the mean.
- **Magnitude of Z**: Indicates how many standard deviations the value \( X \) is from the mean.
