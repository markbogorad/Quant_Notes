up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# TAR Models
**Intuition**: The TAR model allows the relationship between the current and past values of a time series to change based on whether a threshold is crossed (e.g., whether yt−d is above or below τ). It captures regime-dependent dynamics, where the system behaves differently in different states.
$$y_t =
\begin{cases}
\phi_1 y_{t-1} + \varepsilon_t & \text{if } y_{t-d} \leq \tau \\
\phi_2 y_{t-1} + \varepsilon_t & \text{if } y_{t-d} > \tau
\end{cases}$$
- A regime switching model
- Endogenous regime switch (autoregressive)
- Additional TAR family:
	- [[SETAR]]
	- [[STAR]]
