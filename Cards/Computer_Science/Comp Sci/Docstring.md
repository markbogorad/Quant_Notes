up:: [[Python MOC]]
tags:: #Programming 
# Docstring
- **Have no effect on execution of program!!**
	- Essentially another form of commenting
- A special kind of string that is used to document the code and introduce parameters and what you return
- Use at the very beginning of a [[Classes in Python]]
- enclosed in triple quotes (`""" ... """`)
## Example:
```
import math
from scipy.stats import norm

def black_scholes(S, X, T, r, sigma, option_type="call"):
    """
    Calculate the Black-Scholes option price.

    Parameters:
    S : float
        Current stock price
    X : float
        Strike price
    T : float
        Time to maturity (in years)
    r : float
        Risk-free interest rate
    sigma : float
        Volatility of the stock
    option_type : str
        Type of option ("call" or "put")

    Returns:
    float
        The Black-Scholes option price
    """
    d1 = (math.log(S / X) + (r + 0.5 * sigma**2) * T) / (sigma * math.sqrt(T))
    d2 = d1 - sigma * math.sqrt(T)
    
    if option_type == "call":
        option_price = (S * norm.cdf(d1)) - (X * math.exp(-r * T) * norm.cdf(d2))
    elif option_type == "put":
        option_price = (X * math.exp(-r * T) * norm.cdf(-d2)) - (S * norm.cdf(-d1))
    else:
        raise ValueError("option_type must be 'call' or 'put'")
    
    return option_price

# Example usage:
S = 100  # Current stock price
X = 100  # Strike price
T = 1    # Time to maturity (1 year)
r = 0.05 # Risk-free interest rate (5%)
sigma = 0.2  # Volatility (20%)

call_price = black_scholes(S, X, T, r, sigma, option_type="call")
put_price = black_scholes(S, X, T, r, sigma, option_type="put")

print(f"Call Option Price: {call_price:.2f}")
print(f"Put Option Price: {put_price:.2f}")

```

