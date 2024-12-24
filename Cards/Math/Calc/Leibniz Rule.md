up:: [[Calculus MOC]]
tags:: #Math
# Differentiation Under the Integral (Leibniz Rule)
- Used when integrands depend on a parameter
$$I(\alpha) = \int_{a(\alpha)}^{b(\alpha)} f(x, \alpha) \, dx$$
- where $f(x,α)$ is a function that depends on both $x$ and a parameter $α$, and the limits of integration $a(α)$ and $b(α)$ may also depend on $α$. Under certain conditions (continuity and differentiability), the differentiation under the integral sign is given by: (this is Leibniz Rule)
	- $\frac{d}{dx} \int_{a(x)}^{b(x)} f(x, t) \, dt = f(x, b(x)) \frac{d}{dx} b(x) - f(x, a(x)) \frac{d}{dx} a(x) + \int_{a(x)}^{b(x)} \frac{\partial}{\partial x} f(x, t) \, dt$
		- = change ([[Derivatives]]) in upper limit - change in lower limit + the change under the integral ([[Partial Derivatives]])


