up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# Durbin Watson Test
- Assesses the presence of 1st order autocorrelation ([[Serial Correlation]])in the residuals
	- If T is correlated with T-1
- Null: no autocorrelation (want to not reject i.e. high p values)
- Follows it's own distribution (DW table)

## DW test statistic
- Ranges between 0-4
$$ DW = \frac{\sum_{t=2}^{n} (e_t - e_{t-1})^2}{\sum_{t=1}^{n} e_t^2}$$
			- e: residual at time t
- Around 2: no serial correlation
	- ![[Pasted image 20240520122435.png]]
- Approaching 0 (<2): positive serial correlation $\text{Cov}(u_i, u_{i+1}) > 0$
	- ![[Pasted image 20240520122412.png]]
- Approaching 4 (>2): negative serial correlation $\text{Cov}(u_i, u_{i+1}) < 0$
	- ![[Pasted image 20240520122423.png]]
	