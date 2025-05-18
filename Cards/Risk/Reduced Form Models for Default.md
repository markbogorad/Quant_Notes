up:: [[Risk Management MOC]]
tags:: #Finance 
# Reduced Form Models for Default
- Used in actual pricing 
	- Come up with a stochastic process that describes defaults - don't ask why, more so when and what happens if
- Modeling default as a random event regardless of cause
## Poisson $\lambda$ framework
- $\lambda$ is default intensity
$$Pr(N(t)=n)=e^{\lambda t}\frac{(\lambda t)^n}{n!}, E[N(t)]=\lambda t$$
## More Realistic Modeling: Stochastic $\lambda$
- $\lambda$ becomes path dependent ([[Cox, Ingersoll, Ross]])
- Survival probability is essentially the probability that the bond defaults beyond maturity
	- $X(0,T)=P(\tau_1>1)$ where $\tau$ is the first default event
	- Is the same as writing $X(0,T)=E[e^{-\int^T_0 \lambda(u)du}]$
		- Same as time varying $Pe^{-\lambda t}$
### Instantaneous $\lambda$ (Hazard Rate/default spread)
- "If the bond has survived up to time t, what is the likelihood it defaults in the **next instant**?
$$\lambda(t) = \lim_{\Delta t \to 0} \frac{\mathbb{P}(t \leq \tau < t + \Delta t \mid \tau \geq t)}{\Delta t}$$
- where
	- $( \tau )$ is the random default time.
    - $( \mathbb{P}(\cdot))$ is the risk-neutral probability.
    - $( \tau \geq t )$ ensures that we are calculating the intensity given survival up to $( t )$.