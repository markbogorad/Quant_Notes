up:: [[Oil Markets MOC]]
tags:: #Finance 
# Black-Scholes for Futures
### GBM for Futures
$$dF(t,T) = \mu(F,t)dt + \sigma(F,t)dz$$
### Apply [[Ito's Lemma]] for Option on Future
$$dC = \left( \frac{\partial C}{\partial t} + \frac{1}{2} \sigma^2(F,t) \frac{\partial^2 C}{\partial F^2} \right) dt + \frac{\partial C}{\partial F} dF$$
$$= \left( \frac{\partial C}{\partial t} + \mu(F,t) \frac{\partial C}{\partial F} + \frac{1}{2} \sigma^2(F,t) \frac{\partial^2 C}{\partial F^2} \right) dt + \sigma(F,t) \frac{\partial C}{\partial F} dz$$
### Risk Neutral Framework same
$$\Pi(F,t) = C(F,t) - \Delta \cdot F$$
$$d\Pi = \left( \frac{\partial C}{\partial t} + \mu(F,t) \left( \frac{\partial C}{\partial F} - \Delta \right) + \frac{1}{2} \sigma^2(F,t) \frac{\partial^2 C}{\partial F^2} \right) dt + \sigma(F,t) \left( \frac{\partial C}{\partial F} - \Delta \right) dz$$
$$\Delta = \frac{\partial C}{\partial F}$$

## Arrive at PDE
- Since there is no cost to enter futures, the final equation simplifies a little
$$\frac{\partial C}{\partial t} + \frac{1}{2} \sigma^2(F,t) \frac{\partial^2 C}{\partial F^2} - rC = 0$$
