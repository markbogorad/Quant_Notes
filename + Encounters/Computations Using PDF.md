up:: [[Probability MOC]]
tags:: #Math 
# Computations
$\text{Consider a random variable } X \text{ with the probability density function (PDF) defined as:}$ 
	$f_X(x) = \begin{cases} 3x^2, & \text{if } 0 \leq x \leq 1, \\ 0, & \text{otherwise}. \end{cases}$

$\textbf{Goal:} \\ \text{Find the probability }$ $P(X \leq a)$. 
$\textbf{Steps to Solve:}$
1. $\text{Set up the integral to find } P(X \leq a):$ 
		$P(X \leq a) = \int_{-\infty}^{a} f_X(x) \, dx$ 

2. $\text{Break down the integral based on the value of } a:$ $[ P(X \leq a) = \int_{-\infty}^{0} 0 \, dx + \int_{0}^{1} 3x^2 \, dx + \int_{1}^{a} 0 \, dx$

3. $\text{Simplify the integral:} P(X \leq a) = \int_{0}^{1} 3x^2 \, dx$

4. $\text{Evaluate the integral:} \int_{0}^{1} 3x^2 \, dx = \left[ x^3 \right]_{0}^{1} = 1^3 - 0^3 = 1$

5. $\textbf{Conclusion:}$ 
	$\text{- If } a > 1, \text{ then } P(X \leq a) = 1$ 
	$\text{ because the total area under the curve } f_X(x) \text{ from 0 to 1 is 1.}$ 
	$\text{- For } a \text{ within the interval } 0 \leq a \leq 1, \text{ you would evaluate the integral from 0 to } a.$

## General Steps
1. **Identify the PDF**: Understand the function $( f_X(x) )$ that defines the probability distribution of the random variable $( X )$.
2. **Set Up the Integral**: To find the probability that $( X )$ falls within a certain interval $([a, b])$, set up the integral of the PDF over that interval:
	   $P(a \leq X \leq b) = \int_{a}^{b} f_X(x) \, dx$
3. **Break Down the Integral if Necessary**: Depending on the range of integration and the definition of the PDF, you may need to break down the integral into parts, especially if the PDF has different definitions over different intervals.
4. **Evaluate the Integral**: Solve the integral to find the probability. This might involve straightforward integration, applying fundamental calculus techniques.

### Special Cases:
- **Constant PDF**: If the PDF is constant over a certain interval (e.g., the uniform distribution), the integral is simpler and directly proportional to the length of the interval.
- **Piecewise PDF**: Sometimes, the PDF is defined piecewise (as in your example, where $( f_X(x) )$ is $3x^2$ in $([0, 1])$ and 0 otherwise). In such cases, you need to carefully apply the integral to each segment.

