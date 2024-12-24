up:: [[Calculus MOC]]
tags:: #Math
# Integration
- Gives the total accumulation of quantities (i.e. area under the curve)
	- Reverse of [[Derivatives]]
- **Definite Integrals:**
	- Area under the curve $f(x)$ from $x=a$ to $x=b$
	- $\int_a^b f(x) \, dx$
- **Indefinite Integrals**
	- The derivative is the integrand
		- Here, you always add a constant C to account for unknown constants that got anti derived
	- $\int f(x) \, dx$
- Solving
	- Integrate (either antiderivative, substitution, or by parts)
	- Evaluate for the bounds (for definite integrals)
		- $\left[ \frac{x^3}{3} \right]_0^2 = \frac{2^3}{3} - \frac{0^3}{3} = \frac{8}{3} - 0 = \frac{8}{3}​$
		- So, the area under the curve from $x=0$ to $x=2$ is ​$\frac{8}{3}$
## Antiderivative
 $$\int x^n \, dx=\frac{x^{k+1}}{k+1}$$
- Reverse power rule

## Integration by Substitution
- Idea: transform the integral into a simpler function (so you can use antiderivative) by subbing in a temporary $u$ variable
$$u = g(x), \quad du = g'(x) \, dx$$
- Used when integrand is a composite function, essentially the reverse of chain rule
- Steps:
	- Set a $u$ variable, usually the inner function of the composite function
	- Compute the [[Derivatives]] of u
		- If $u=g(x)$, then $du=g′(x) dx$.
	- Substitute $u$ and $du$ back into the integral
	- Preform integration with respect to $u$
	- Substitute back the original $x$
	
- Example: $\int 2x{{e^x}^2}$
	- $u = x^2$
	- so, $du = 2x$
	- Substitute --> $\int 2x{{e^x}^2} = \int e^u du$
	- Integrate with respect to u --> $\int e^u du = e^u + C$
	- Sub back x --> $e^u + C = e^{{x}^2}$


## Integration by Parts
- Used when computing the product of integrals, the reverse of product rule
$$ \int u \, dv = uv - \int v \, du$$
- $u$ is a function you choose to differentiate $(du=u'dx)$
- $du$ is a function you choose to integrate $(v=\int dv)$
- Steps:
	- Choose parts of the integrand to be $u$ and $dv$.
	- Compute $du$: Differentiate $u$ to find $du$.
	- Compute $v$: Integrate $dv$ to find $v$.
	- Substitute into the Formula: Substitute $u$, $du$, $v$, and $dv$ into the integration by parts formula.
	- Simplify and Integrate: Simplify the resulting expression and integrate if necessary.
	
- Example: $\int x{{e^x}}dx$
	- $u = x$ (easy to derive)
		- $du$ = $dx$
	- so, $dv = e^x$ (easy to integrate)
		- $v$ = $e^x$
	- Substitute into the integration by parts formula --> $\int x \, e^x dx = xe^x - \int e^x \, dx$
	- Solve
		- $xe^x - \int e^x \, dx$
			- integral of $\int e^x \, dx$ is just $e^x$
				- $= xe^x -e^x + C$
	