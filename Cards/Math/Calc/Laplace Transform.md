up:: [[Calculus MOC]]
tags:: #Math
# Laplace Transform
- Converts [[Differential Equations MOC]] into algebraic equations
- Also:
- Used to transform a **function of time** $f(t)$ into **a complex variable** $s$ or vice versa with inverse
	- Used in practice to solve complex PDEs easier by simplifying the derivation
	- Can be used to:
		- Model the [[Term Structure of Interest Rates]]
		- Specific option pricing with [[Black-Scholes]]
		- [[Credit Risk]] modeling
- The Laplace transform of a function $( f(t) )$, defined for $( t \geq 0 )$, is given by: $$[ \mathcal{L}\{f(t)\} = F(s) = \int_0^\infty e^{-st} f(t) \, dt ] \hspace{1cm} OR \hspace{1cm} F(s) = \int_{0}^{\infty} f(t) e^{-st} \, dt$$
	- Here, $( s )$ is a complex number, $( s = \sigma + i\omega )$, where $( \sigma )$ and $( \omega )$ are real numbers.
## Common Pairs:
- ![[Pasted image 20240701152703.png]]


## Laplace Transforms to solve [[ODE]]
- How to solve:
	- Apply Laplace to both sides of equation, this converts derivatives into algebraic terms
	- Solve the new algebraic equation
	- Convert back to get original function (inverse Laplace)

- Key properties --> this is how you transform the ODE into an algebraic equation
	- $L{y′′}=s^2Y(s)−sy(0)−y′(0)$
	- $L{y′}=sY(s)−y(0)$
	- $L{y}=Y(s)$
	- $L^{e−t}=\frac{1}{s+1}$ 
		- This is inverse laplace



- ![[Pasted image 20240705141608.png]]
