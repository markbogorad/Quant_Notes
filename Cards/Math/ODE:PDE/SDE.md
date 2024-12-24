up:: [[Differential Equations MOC]], [[Stochastic Calculus MOC]]
tags:: #Math
# Stochastic Differential Equations
- Stochastic differential equations (SDEs) are used to model systems that are influenced by random processes.
- An SDE typically has the form: $dXt=f(Xt,t)dt+g(Xt,t)dWt$
	- where:
		- $X_t$​ is the state variable.
		- $f(X_t,t)$ is the drift term, representing deterministic trends. 
			- describes the average rate of change of the process over time.
		- $g(X_t,t)$ is the diffusion term, representing stochastic effects. 
			- describes the intensity of the random fluctuations.
			- $dW_t$​ is an increment of the Wiener process, which has mean zero and variance dtdt.
		- $W_t$​ is a Wiener process or Brownian motion, representing the random noise.