up:: [[Numerical Methods MOC]]
tags:: #Math 
# Adaptive Step Sizing
- Instead of using a fixed step size h, we dynamically adjust h based on the error estimate.
- $x_h$​ = Solution using step size $h$.
- $x_{2h}$​ = Solution using a larger step size $2_h$.
	- $x(t + 2h) = x_h(t + 2h) + 2h^5 \varphi + O(h^6)$
	- $x(t + 2h) = x_{2h}(t + 2h) + (2h)^5 \varphi + O(h^6)$
- If the step is **too large**, the error increases, so we **reduce h**.
- If the step is **too small**, we **increase h** to speed up computation.
## In [[Runge-Kutta Methods]]
$$\Delta = x_{2h}(t+2h) - x_h(t+2h) = 30 h^5 \varphi + O(h^6)$$
- Step Size Adjustment Rule
- If $( |\Delta| )$ is too large: $h \to \frac{h}{2}$ 
- If $( |\Delta| )$ is too small: $h \to 2h$
- **Increases efficiency** by making large steps where possible.
- **Maintains accuracy** by reducing step size in tricky regions.