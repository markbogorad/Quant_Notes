up:: [[Probability MOC]]
tags:: #Math
# Multivariate Distribution Theory
- The study of [[Random Variables]] taking on multiple values simultaneously
	- Modeled with [[Joint Distributions (Discrete vs Continuous)]]
- A multivariate random variable is a **vector of two or more random variables**
### Key Concepts:
1. **Multivariate [[Random Variables]]:
   - A multivariate random variable is **a vector of two or more random variables**. For example, if $( X_1, X_2, \dots, X_n )$ are random variables, their combination $( \mathbf{X} = (X_1, X_2, \dots, X_n) )$ forms a multivariate random variable.
   
2. [[Joint Distributions (Discrete vs Continuous)]]:
   - The joint probability distribution of a multivariate random variable describes the probability that each of the individual random variables takes on a specific value simultaneously.
   - For continuous random variables, the joint probability density function (PDF) $( f_{\mathbf{X}}(\mathbf{x}) )$ gives the likelihood of the vector $( \mathbf{X} )$ taking on the values $( \mathbf{x} = (x_1, x_2, \dots, x_n) )$.

3. [[Marginal Distribution]]:
   - The marginal distribution of a subset of variables from a multivariate distribution is the probability distribution of that subset, obtained by integrating or summing out the other variables.
   - For example, if $( f_{X,Y}(x,y) )$ is the joint PDF of $( X )$ and $( Y )$, the marginal PDF of $( X )$ is obtained by integrating out $( Y )$:
     $f_X(x) = \int_{-\infty}^{\infty} f_{X,Y}(x,y) \, dy$

4. **Conditional Distributions**:
   - The conditional distribution of one variable given another is derived from the joint distribution. It describes the distribution of one variable given that the other variable takes on a specific value.
   - For example, the conditional PDF of \( X \) given \( Y = y \) is:
     $f_{X|Y}(x|y) = \frac{f_{X,Y}(x,y)}{f_Y(y)}$

5. **Covariance and Correlation**:
   - [[Covariance]] measures the degree to which two random variables vary together. For random variables \( X \) and \( Y \):
     $\text{Cov}(X, Y) = E[(X - E[X])(Y - E[Y])]$
   - [[Correlation]] is a normalized version of covariance, providing a dimensionless measure of the linear relationship between variables, ranging from -1 to 1.

6. **Multivariate Normal Distribution**:
   - A key distribution in multivariate theory is the multivariate normal (Gaussian) distribution. A random vector \( \mathbf{X} = (X_1, X_2, \dots, X_n) \) is multivariate normal if every linear combination of its components is normally distributed.
   - The PDF of a multivariate normal distribution is given by:
     $f_{\mathbf{X}}(\mathbf{x}) = \frac{1}{(2\pi)^{n/2} |\Sigma|^{1/2}} \exp\left(-\frac{1}{2}(\mathbf{x} - \mu)^T \Sigma^{-1} (\mathbf{x} - \mu)\right)$
     where \( \mu \) is the mean vector, \( \Sigma \) is the covariance matrix, and \( |\Sigma| \) is the determinant of \( \Sigma \).

7. **Independence**:
   - In a multivariate context, random variables are independent if their joint distribution is the product of their marginal distributions. That is, \( X_1 \) and \( X_2 \) are independent if:
     $f_{X_1, X_2}(x_1, x_2) = f_{X_1}(x_1) \cdot f_{X_2}(x_2)$
### Applications:
- **Risk Management**: Multivariate distributions are used to model the joint behavior of multiple financial assets, allowing for portfolio optimization and risk assessment.
- [[Machine Learning Miscellaneous MOC]]: Multivariate distributions underpin many algorithms, such as Gaussian mixture models and [[PCA]]
- **Econometrics**: Used to model relationships between economic variables, such as inflation and unemployment rates.

