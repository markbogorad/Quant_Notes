up:: [[Calculus MOC]],   [[Derivatives MOC]]
tags:: #Finance #Math 
# Numerical Integration (Math Portion)
- A method used to approximate the value of definite integrals, especially when an exact analytical solution is difficult or impossible to obtain
## Common Techniques
### Reimann Sums
- Most basic approach --> solve area under curve using the *sum of rectangular series*
- Left Reimann sum
	- Use left point of each subinterval to determine rectangle height
	- $\sum_{i=0}^{n-1} f(x_i) \Delta x$
- Right Reimann sum
	- Use right point of each subinterval to determine rectangle height
	- $\sum_{i=1}^{n} f(x_i) \Delta x$
- Midpoint Reimann sum
	- Use midpoint of each subinterval
	- $\sum_{i=0}^{n-1} f\left(\frac{x_i + x_{i+1}}{2}\right) \Delta x$
### Newton-Cotes Quadrature Rules
**Trapezoidal Rule**
- Approximates area under curve using the *sum of trapezoidal series*
	- More accurate then Reimann sums --> better captures the slope of each function over each interval
- $\int_a^b f(x) \, dx \approx \frac{\Delta x}{2} \left[ f(x_0) + 2 \sum_{i=1}^{n-1} f(x_i) + f(x_n) \right]$

**Simpsons Rule**
- Approximates area under curve using parabolic segments
	- Usually better than trapezoidal rule
- $\int_a^b f(x) \, dx \approx \frac{\Delta x}{3} \left[ f(x_0) + 4 \sum_{i=1,3,5,\ldots}^{n-1} f(x_i) + 2 \sum_{i=2,4,6,\ldots}^{n-2} f(x_i) + f(x_n) \right]$

### Gaussian Quadrature
- Most advanced method, best for smooth functions
- Provides exact results for polynomials of degree up to $2n−1$ using $n$ points and corresponding weights.
- $\int_a^b f(x) \, dx \approx \sum_{i=1}^{n} w_i f(x_i)$

## Steps in Numerical Integration

1. **Divide the Interval**: Choose the number of subintervals $n$ and divide the interval $[a,b]$ into $n$ equal parts, where each subinterval has width $Δx=b−a$​.
    
2. **Evaluate the Function**: Calculate the function values at the chosen points (endpoints, midpoints, or Gaussian points).
    
3. **Apply the Formula**: Use the appropriate numerical integration formula to sum the areas of the shapes.
    
4. **Estimate the Error**: Determine the error of the approximation, which decreases as $n$ increases or by using more sophisticated methods like Simpson’s rule or Gaussian quadrature.

## Example:
Using the trapezoidal rule to approximate the integral of $f(x) = x^2 \text{ from } x = 0 \text{ to } x = 2 \text{ with } n = 4$

Divide the Interval: 
$[0, 2] \text{ into 4 parts: } \Delta x = \frac{2 - 0}{4} = 0.5.$

Evaluate the Function: 
$f(0) = 0^2 = 0, \quad f(0.5) = (0.5)^2 = 0.25, \quad f(1) = 1^2 = 1, \quad f(1.5) = (1.5)^2 = 2.25, \quad f(2) = 2^2 = 4.$

Apply the Formula:
$\int_0^2 x^2 \, dx \approx \frac{0.5}{2} \left[ f(0) + 2(f(0.5) + f(1) + f(1.5)) + f(2) \right]$

$\approx \frac{0.5}{2} \left[ 0 + 2(0.25 + 1 + 2.25) + 4 \right]$

$\approx 0.25 \left[ 0 + 2(3.5) + 4 \right]$

$\approx 0.25 \left[ 7 + 4 \right] = 0.25 \times 11 = 2.75$

So, the approximate value of the integral is 2.75.