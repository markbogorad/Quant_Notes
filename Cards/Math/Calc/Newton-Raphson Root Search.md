up:: [[Calculus MOC]]
tags:: #Math
# Newton Raphson
- A powerful technique for finding successively better approximations to the roots (or zeroes) of a real-valued function
	- Iterative algorithm that uses linear approximation
- The fundamental idea behind the Newton-Raphson method is to **start with an initial guess** for the root of the function, and then **refine that guess iteratively** using the derivative of the function
$$x_{n+1} = x_n - \frac{f(x_n)}{f'(x_n)}$$
- $xn$​ is the current guess for the root.
- $f(x_n​)$ is the value of the function at $x_n$​.
- $f′(x_n​)$ is the value of the derivative of the function at $x_n$​.
- $xn+1​$ is the next, improved guess.

### Steps to Implement the Newton-Raphson Method

1. **Choose an Initial Guess** ($x_0​$): This should be as close as possible to the actual root, based on the behavior of the function or previous knowledge.
2. **Evaluate the Function and Its Derivative**: Compute $f(x_0)$ $f′(x_0)$.
3. **Update the Guess**: Use the formula to find a new guess $x_1$​, (above)
4. **Repeat Until Convergence**: Continue updating the guess according to the Newton-Raphson formula until the changes in the guesses are within a pre-defined tolerance level, or the maximum number of iterations is reached.