up:: [[Calculus MOC]]
tags:: #Math
# Taylor Series
- A way to represent a function as an *infinite sum of terms* calculated from the values of its derivatives at a single point
	- It is an infinite series, but you put a stop to it when accurate enough
- Used for approximating otherwise very hard to solve functions
	- Taking non polynomials and using polynomials to try and reproduce the non polynomial
- The more terms you choose, the better the approximation
	- In exchange, you make the polynomial more complicated
	
$$f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x-a)^n $$
In practice:
$$f(x) \approx f(a) + f'(a)(x-a) + \frac{f''(a)}{2!}(x-a)^2 + \frac{f'''(a)}{3!}(x-a)^3 + \frac{f^{(4)}(a)}{4!}(x-a)^4 + \ldots + \frac{f^{(n)}(a)}{n!}(x-a)^n + \ldots$$
- where
	- $f^{(n)}(a)$ is the n-th derivative of $f(x)$ evaluated at the point $a$.
	- $n!$ (n factorial) is the product of all positive integers up to $n$.
	- $a$ is what we are analyzing the Taylor series around
	

- Taylor series in [[Stochastic Calculus MOC]] is [[Ito's Lemma]]