up:: [[Differential Equations MOC]]
tags:: #Math
# Integrating Factor Solution (ODEs)
- *Logic:* you want to solve for y in terms of x, but the term $p(x)y$ complicates this. So we bring in an **integrating factor** to make it integratabtle 
- For first order [[ODE]] only
- The integrating factor method is a technique used to solve linear **first-order ordinary differential equations** of the form:
$$y′+p(x)y=q(x)$$
				-y' is the same as $\frac{dy}{dx}$
## Solving:
1) Compute the integrating factor, given by
	- $μ(x)=e^{∫p(x)dx}$
		- new variable
		
2) Multiply through by the Integrating Factor $(u(x))$
	- Multiply both sides of the original differential equation by $μ(x)$:
		- $μ(x)y′+μ(x)p(x)y=μ(x)q(x)$
	- Since $μ(x)$ is chosen to make the left-hand side a product of the derivative, the equation can be rewritten as:
	
3) Integrate both sides
	- $∫\frac{d}{dx}​(μ(x)y)dx=∫μ(x)q(x)dx$
	- Simplifies to:
	- $μ(x)y=∫μ(x)q(x)dx+C$
	
4) Solve for the variable of interest (Y)
	- Solve for $y$ by dividing both sides by $μ(x)$:
	- $y=\frac{1}{μ(x)}(∫μ(x)q(x) dx+C)y$
		- $=μ(x)1​(∫μ(x)q(x)dx+C)$

### Example

Given the first-order linear ordinary differential equation:

	$y' - 2y = e^{2x}$



**Step 1: Identify the equation**

The given equation is in the form:

	$y' + p(x)y = q(x)$

Here, $( p(x) = -2 )$ and $( q(x) = e^{2x} )$.



**Step 2: Compute the Integrating Factor**

The integrating factor, $( \mu(x) )$, is given by:

$\mu(x) = e^{\int p(x) \, dx} = e^{\int -2 \, dx} = e^{-2x}$



**Step 3: Multiply through by the Integrating Factor**

Multiply both sides of the original differential equation by $( \mu(x) )$:

$e^{-2x} y' - 2e^{-2x} y = e^{-2x} e^{2x}$

This simplifies to:

$e^{-2x} y' - 2e^{-2x} y = 1$

Rewrite the left-hand side as a derivative:

$\frac{d}{dx} \left( e^{-2x} y \right) = 1$



**Step 4: Integrate Both Sides**

Integrate both sides with respect to $( x )$:

$\int \frac{d}{dx} \left( e^{-2x} y \right) \, dx = \int 1 \, dx$

This simplifies to:

$e^{-2x} y = x + C$



**Step 5: Solve for $( y )$**

Solve for $( y )$ by multiplying both sides by $( e^{2x} )$:

$y = e^{2x} (x + C)$

Thus, the solution to the differential equation $( y' - 2y = e^{2x} )$ is:

$y = e^{2x} (x + C)$

where $( C )$ is an arbitrary constant.


