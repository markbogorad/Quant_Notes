up:: [[Probability MOC]]
tags:: #Math
# Exponential Distribution
- Waiting time between periods in the [[Poisson Distribution]] process ecents
	- Pausing time between occurrence of events
### Key Characteristics:
- **Rate Parameter** $( \lambda )$: The parameter $( \lambda )$ is known as the rate parameter. It represents the average number of events per unit time and is the inverse of the mean. 
	- A larger $( \lambda )$ indicates that events happen more frequently, while a smaller $( \lambda )$ indicates they happen less frequently.
- **Support**: The random variable $( X )$ takes values in the interval $([0, \infty))$

### Probability Density Function (PDF):
- The [[Probability Density Function (PDF)]] of an Exponential distribution is defined as:
$$
f_X(x) =
\begin{cases}
\lambda e^{-\lambda x}, & \text{if } x \geq 0, \\
0, & \text{if } x < 0.
\end{cases}
$$
### Notation:
The Exponential distribution with rate parameter \( \lambda \) is denoted as:
$$X \sim \text{Exp}(\lambda)$$
### Cumulative Distribution Function (CDF):
The [[Cumulative Distribution Function (CDF)]] of the Exponential distribution, which gives the probability that the random variable $( X )$ is less than or equal to a certain value $( x )$, is given by:
$$F_X(x) = 1 - e^{-\lambda x}, \quad \text{for } x \geq 0$$
### Mean (Expected Value):
The mean (expected value) of an Exponential distribution is the inverse of the rate parameter \( \lambda \):
$$E[X] = \frac{1}{\lambda}$$
### Variance:
The variance of an Exponential distribution is the inverse of the square of the rate parameter \( \lambda \):
$$\text{Var}(X) = \frac{1}{\lambda^2}$$
### Key Properties:
- **Memoryless Property**: One of the most unique and important properties of the Exponential distribution is that it is memoryless. Formally, this means:
  $$P(X > s + t \mid X > s) = P(X > t)$$
  - This property implies that the probability of an event occurring in the future is **independent of the past.****
### Example:
$$\textbf{Given:} \\
f(t) = \frac{1}{15} \exp\left(-\frac{t}{15}\right), \quad t > 0$$

$$\textbf{Find:} \\
P(15 < T < 30)$$

$$\textbf{Solution:} \\
P(15 < T < 30) = \int_{15}^{30} \frac{1}{15} \exp\left(-\frac{t}{15}\right) \, dt$$

$$\textbf{Step 1: Integral:} \\
P(15 < T < 30) = \int_{15}^{30} \frac{1}{15} \exp\left(-\frac{t}{15}\right) \, dt$$

$$\textbf{Step 2: Evaluate:} \\
\int \frac{1}{15} \exp\left(-\frac{t}{15}\right) \, dt = -\exp\left(-\frac{t}{15}\right)$$

$$P(15 < T < 30) = \left[-\exp\left(-\frac{t}{15}\right)\right]_{15}^{30}$$

$$\textbf{Step 3: Substitute:} \\
P(15 < T < 30) = -\exp\left(-\frac{30}{15}\right) + \exp\left(-\frac{15}{15}\right)$$

$$P(15 < T < 30) = -\exp(-2) + \exp(-1)$$

$$P(15 < T < 30) = -e^{-2} + e^{-1} \approx -0.1353 + 0.3679 = 0.2325$$
