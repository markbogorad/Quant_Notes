up:: [[Numerical Methods MOC]]
tags:: #Math 
# Heat Equation
$$\frac{\partial u}{\partial t} = \alpha \frac{\partial^2 u}{\partial x^2}, \quad \alpha > 0$$
- A fundamental [[PDE]] that describes how heat diffuses through a medium over time
- **Initial Condition**:
    - Specifies the temperature distribution at $t=0, u(x,0)=f(x)$.
- **Boundary Conditions** (examples):
    - **Dirichlet**: $u(0,t)=A$ and $u(L,t)=B$ (fixed temperatures at the boundaries).
    - **Neumann**: $\frac{∂u}{∂x}(0,t)=0$ (insulated boundaries).
### Relationship to [[Black-Scholes]]
- The Black-Scholes equation can be transformed into the heat equation through a change of variables. 
- leverage known solutions of the heat equation to solve Black-Scholes and better understand its properties.
#### Heat equation to Black-Scholes

The Black-Scholes partial differential equation is:

$$\frac{\partial V}{\partial t} + \frac{1}{2} \sigma^2 S^2 \frac{\partial^2 V}{\partial S^2} + rS \frac{\partial V}{\partial S} - rV = 0$$

with the boundary condition:

$$
V(S, T) = \max(S - K, 0)
$$

To solve this PDE, we introduce the following change of variables:

- $( x = \ln(S))$ (logarithmic transformation)
- $( \tau = T - t)$ (reverse time)
- $( V(S, t) = e^{\alpha x + \beta \tau} u(x, \tau))$

The goal is to simplify the Black-Scholes PDE into a standard heat equation:
$$
\frac{\partial u}{\partial \tau} = \frac{\partial^2 u}{\partial x^2}
$$
The solution of the heat equation is well-known and given by:

$$
u(x, \tau) = \frac{1}{\sqrt{4\pi \tau}} \int_{-\infty}^{\infty} e^{-\frac{(x-y)^2}{4\tau}} f(y) \, dy
$$

where $( f(y) )$ represents the initial condition for $( u(x, 0) )$.
Once the solution $( u(x, \tau) )$ is obtained, we transform it back to the original variables:

- $( x = \ln(S))$
- $( \tau = T - t )$
- $( V(S, t) = e^{\alpha x + \beta \tau} u(x, \tau))$
The closed-form solution for the European call option price is:

$$
C(S, t) = S N(d_1) - Ke^{-r(T-t)} N(d_2)
$$
where:

$$
d_1 = \frac{\ln\left(\frac{S}{K}\right) + \left(r + \frac{\sigma^2}{2}\right)(T-t)}{\sigma \sqrt{T-t}}, \quad d_2 = d_1 - \sigma \sqrt{T-t}
$$

$( N(\cdot) )$ is the cumulative normal distribution function.
## Solutions to the Heat Equation
### Separation of Variables Solution
- [[Separation of Variables]]
### Solution via Fourier Transform
- [[Fourier Transforms]]
### Finite Difference Methods
- [[Finite Difference Methods]]
	- [[Explicit FTCS FDM]]
	- [[Fully Implicit FDM]]
	- [[Crank Nicholson]]