up:: [[Stochastic Calculus MOC]],    [[Oil Markets MOC]]
tags:: #Math 
# Diffusions
$$dF=\mu(F,t)dt+\sigma(F,t)dz$$
- A [[Stochastic Process]] and a specific type of [[PDE]]
	- Whereas a stochastic differential equation ([[SDE]]) is a type of [[ODE]]
	- Key difference: diffusion equations are multi-dimensional and SDEs are single dimensional 
		- [[Geometric Brownian Motion]] and [[Arithmetic Brownian Motion]] are special cases of single dimension diffusions, AKA SDEs
- $\sigma(F,t)$ characterizes the volatility of the diffusion process, AKA [[Local Volatility]]
- **Key characteristic in oil**: volatility is not constant and is simulated ([[Simulation in Finance]])
### GBM and ABM vs Diffusion

| **Aspect**           | **ABM/GBM**                                                                    | **Stochastic Diffusion Equation**              |
| -------------------- | ------------------------------------------------------------------------------ | ---------------------------------------------- |
| **Equation Type**    | Stochastic Differential Equation (SDE)                                         | Stochastic Partial Differential Equation (PDE) |
| **Scope**            | Temporal stochastic evolution                                                  | Spatial and temporal stochastic evolution      |
| **Dimensionality**   | Single variable $(Xt​)$ in time                                                | Fields $u(x,t))$ in space and time             |
| **Random Component** | Brownian motion $(dWt​)$                                                       | Random noise $η(x,t))$ in space and time       |
| **Examples**         | ABM: $dXt=μdt+σdWtdXt​=μdt+σdWt$​; GBM: $dXt=μXtdt+σXtdWtdXt​=μXt​dt+σXt​dWt$​ | Heat equation with stochastic noise            |