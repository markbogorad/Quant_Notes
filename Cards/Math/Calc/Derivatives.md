øup:: [[Calculus MOC]]
tags:: #Math
# Derivatives
- The rate at which a function is changing at any given point in time
	- ***$\frac{df}{dx}$ : the rate at which function f changes as variable x changes***
- Slope of the tangent line to the curve representing whatever you are examining
![[intro_1.png]]
- Slope of orange line is the derivative
## Rules
- **Exponential** 
	- $\frac{d}{dx}(e^x) = e^x$
	- Do not do $x-1$ with exponentials
- **Natural Logarithm**
	- $\frac{d}{dx}(\ln(x)) = \frac{1}{x} \quad \text{for } x > 0$
- **When differential is in exponent: use log transformation [[Logarithms]]**
	- $\frac{d}{dx}(a^x) = e^{xln(a)}$ 
- **Square Root**
	- $\frac{d}{dx}\sqrt{x} = x^{1/2} = \frac{1}{2} x^{-1/2} = \frac{1}{2 \sqrt{x}}$
### Single Function Operations
- **Constant Rule**
	- $\frac{d}{dx}[c] = 0$
	- Derivative of a constant is 0
- **Constant Multiple Rule**
	- $\frac{d}{dx}[cf(x)] = c \cdot f'(x)$
	- Derivative of a constant times a function is the constant times the derivative of the function (*only derive the function*)
- **Power Rule**
	- **$\frac{d}{dx}[x^n] = nx^{n-1}$
	- Bring down exponent to front, take 1 away from exponent 
- **Sum and Difference Rules**
	- $\frac{d}{dx}[f(x) + g(x)] = f'(x) + g'(x)$   and    $\frac{d}{dx}[f(x) - g(x)] = f'(x) - g'(x)$
	- The derivative of a sum or difference is the sum or difference of the derivatives.

### Multiple Function Operations
- **Chain Rule**
	- Used for composite functions
	- $\frac{d}{dx} f(g(x)) = f'(g(x)) \cdot g'(x)$
		- Solved by setting 2 components
			- a `u` value to represent `g(x)` and a `h(x)` value to represent `f(x)`
	- Example: $\frac{d}{dx}[(3x^2 + 2)^5]$
		- Let $u=3x^2+2$, so $h(x)=u^5$
		- $5(3x^2 + 2)^4 \cdot 6x$
			- Derivative of outside * regular inside * derivative of inside
			
- **Product Rule**
	- Used for products of two functions
	- $\frac{d}{dx}[f(x)g(x)] = f'(x)g(x) + f(x)g'(x)$

- **Quotient Rule**
	- Used for quotient of two functions
	- $\frac{d}{dx} \left[\frac{f(x)}{g(x)}\right] = \frac{f'(x)g(x) - f(x)g'(x)}{[g(x)]^2}$
		- Product rule / g(x)^2

When a problem is more complex, use [[Implicit Differentiation]]