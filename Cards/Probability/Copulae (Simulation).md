up:: [[Quantitative Valuation MOC]]
tags:: #Finance  
# Copulae
- A special cases of [[Multivariate Simulation (Correlating Cash Flows)]]
- A copula allows you to model statistical dependencies between variables
	- They allow you to model the dependence structure between variables separately from their marginal distributions.

## Valuation Exercise
The goal of the exercise is to:

1. **Correlate two uniform random variables**.
2. **Transform these correlated uniform variables into correlated exponential variables** with specific parameters (0.2 and 0.3).
3. **Visualize the results** by creating scatterplots, one showing zero correlation and one showing 80% correlation.

### Steps to Complete the Exercise

1. **Simulate Uncorrelated Normal Numbers**:
    
    - Start by generating two independent standard normal variables (with mean 0 and variance 1). These will be the basis for generating correlation.
2. **Force a Correlation (Moment Matching)**:
    
    - Use a technique such as the **Cholesky decomposition** to impose a desired correlation on these normal variables.
    - For example, to achieve 80% correlation, you would adjust these variables so that the correlation coefficient between them is 0.8.
3. **Convert to Uniform (Result: “Correlated” Uniforms)**:
    
    - Apply the **cumulative distribution function (CDF)** of the standard normal distribution to each of these correlated normal variables. This will convert the normally distributed values to uniformly distributed values between 0 and 1, but they’ll still retain the correlation structure.
    - This step results in two correlated uniform random variables.
4. **Convert to Correlated Exponentials Using the Inverse CDF (Quantile Function)**:
    
    - To convert the correlated uniform variables into correlated exponential variables, apply the **inverse CDF (quantile function)** of the exponential distribution.
    - If the exponential distributions have parameters λ1=0.2λ1​=0.2 and λ2=0.3λ2​=0.3, then for each correlated uniform variable UU, you transform it into an exponential variable using the formula:X=F−1(U)=−ln⁡(1−U)λX=F−1(U)=−λln(1−U)​
    - This transformation gives you two correlated exponential variables with the desired parameters and the same correlation as the original uniform variables.
5. **Graph**:
    
    - Plot the resulting exponential variables in scatterplots to visualize their correlation.
    - Create one plot for zero correlation and another plot for 80% correlation to observe how the dependence structure changes.