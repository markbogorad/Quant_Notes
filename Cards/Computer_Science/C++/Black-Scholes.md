up:: [[Numerical Methods MOC]], [[Derivatives MOC]]
tags:: #Math #Finance 
# The Black-Scholes Model
The **Black-Scholes equation** is a fundamental partial differential equation (PDE) used to model the price of European-style options. It assumes that the underlying asset follows a [[Geometric Brownian Motion]] with constant volatility and interest rate.

### Black-Scholes [[PDE]]
- Comes from [[Ito's Lemma]]
$$\frac{\partial V}{\partial t} + \frac{1}{2} \sigma^2 S^2 \frac{\partial^2 V}{\partial S^2} + rS \frac{\partial V}{\partial S} - rV = 0$$
Where:  
- $( V(S,t) )$ = option price as a function of the underlying asset $( S )$ and time $( t )$  
- $( \sigma )$ = volatility of the underlying asset  
- $( r )$ = risk-free interest rate  
- $( S )$ = underlying asset price  
- $( t )$ = time to maturity  
### Initial Condition
- For a European call option with strike price \( K \) and maturity \( T \):
$$V(S, T) = \max(S - K, 0)$$
- This defines the option payoff at maturity.
### Boundary Conditions
- $( V(0, t) = 0)$ (Option value is zero when the underlying price is zero)
- $( V(S, t) \to S )$ as $(S \to \infty)$ (Option value approaches the underlying price for very large \( S \))
### Solution (Closed-Form Formula for a European Call)
$$C(S, t) = S N(d_1) - Ke^{-r(T-t)} N(d_2)$$
Where:
$$d_1 = \frac{\ln\left(\frac{S}{K}\right) + \left(r + \frac{\sigma^2}{2}\right)(T-t)}{\sigma\sqrt{T-t}}, \quad d_2 = d_1 - \sigma\sqrt{T-t}$$
$( N(\cdot) )$ is the cumulative distribution function of the standard normal distribution.

## Full Derivation
#### 1) Start with the assumption that the stock follows [[Geometric Brownian Motion]]
$$dSt=μS_t d_t+σS_t dW_t$$
Where:
- $μ$ = drift (expected return)
- $σ$ = volatility
- $W_t$​ = standard Brownian motion
#### 2) Apply [[Ito's Lemma]] to express the dynamics of the option price V(S,t).
- Take the assumption that stock price follows a GBM and expand this onto the option - the option will be the sum of partial derivatives relevant to pricing, these are option value w.r.t. time, stock price, and 2nd order stock price

$$dV=\frac{∂V}{∂t} dt+\frac{∂V}{∂S} dS+\frac{1}{2}\frac{∂^2V}{∂S^2}(dS)^2$$
- We know from the stock’s dynamics that:
$$dSt=μSt dt+σSt dWt$$
Substitute this into $dV$:
$$dV=\frac{∂V}{∂t} dt+\frac{∂V}{∂S} (μS dt+σS dWt)+\frac{1}{2}\frac{∂^2V}{∂S^2}(σ^2S^2dt)^2$$

After substituting and simplifying, $dV$ is expressed in terms of $dt$ and $dW_t$​.
#### Eliminate randomness ($dW_t$) by constructing a risk-neutral portfolio and applying the no-arbitrage principle. This gives the Black-Scholes PDE.
- Construct a self financing portfolio with
	- A long position in the stock (ΔS)
	- A short position in the option (−V)
$$Π=ΔS−V$$
$$dΠ=ΔdS−dV$$
- Substitute in previously defined values
	- $dS=μSd_t+σSdW_t​$ (the stock’s stochastic differential equation)
	- $dV=\frac{∂V}{∂t} dt+\frac{∂V}{∂S} dS+\frac{1}{2}\frac{∂^2V}{∂S^2}(dS)^2$ (Itô’s Lemma applied to the option price)
	- $dV = \frac{\partial V}{\partial t} dt + \mu S \frac{\partial V}{\partial S} dt + \frac{1}{2} \sigma^2 S^2 \frac{\partial^2 V}{\partial S^2} dt + \sigma S \frac{\partial V}{\partial S} dW_t$
- Cancel $dW_t$ by defining [[Delta]] as $\frac{∂V}{∂S}$
	- At the end of the equation, the bit $(Δ−\frac{∂S}{∂V}​)σSd$ will effectively cancel out (multiplied by 0)
- With Delta defined, the portfolio is effectively risk free and must earn the risk free rate R
	- $dΠ=(−\frac{∂t}{∂V}​−\frac{1}{2}​σ^2S^2\frac{∂S2}{∂2V}​)dt$
	- $dΠ=rΠdt$
- Substitute to get the PDE
	- Substitute $Π=ΔS−V=\frac{∂V}{∂S}S−V$ into $dΠ=rΠ dt$, and after some algebra, you get the Black-Scholes PDE:
$$\frac{\partial V}{\partial t} + \frac{1}{2} \sigma^2 S^2 \frac{\partial^2 V}{\partial S^2} + rS \frac{\partial V}{\partial S} - rV = 0$$
#### Solve the PDE using standard methods (transform it into a heat equation).
$$\frac{\partial V}{\partial t} + \frac{1}{2} \sigma^2 S^2 \frac{\partial^2 V}{\partial S^2} + rS \frac{\partial V}{\partial S} - rV = 0$$
- Has initial condition: $V(S,T)=max(S−K,0)$
- Ways to solve
	- Analytically by transforming it into the [[Heat Equation]]
	- [[Finite Difference Methods]]: [[Crank Nicholson]], [[Explicit FTCS FDM]],  [[Fully Implicit FDM]]
	- [[Monte-Carlo Simulation]]
	- [[Trees (Numerical Methods)]]
	- [[Laplace Transform]]
	- [[Fourier Transforms]]
#### When to Use Each Method:

|**Method**|**Best For**|**Complexity**|
|---|---|---|
|Analytical (Heat Equation)|Simple European options|Low|
|Finite Difference|American/exotic options, early exercise|Medium|
|Monte Carlo Simulation|Path-dependent options, multi-dimensional|High|
|Binomial Trees|American options, intuitive explanation|Medium|
|Semi-Analytical|Barrier options, stochastic volatility models|High|