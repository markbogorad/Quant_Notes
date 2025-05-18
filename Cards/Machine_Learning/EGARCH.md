up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# EGARCH
$$\ln(h_t) = \omega + \beta \ln(h_{t-1}) + \alpha \frac{\varepsilon_{t-1}}{\sqrt{h_{t-1}}} + \gamma \left[ \left| \frac{\varepsilon_{t-1}}{\sqrt{h_{t-1}}} \right| - E\left| \frac{\varepsilon_{t-1}}{\sqrt{h_{t-1}}} \right| \right]$$
The EGARCH model uses logarithmic variance, ensuring that the conditional variance is always positive without requiring parameter restrictions. It also captures asymmetric effects, where positive and negative shocks influence volatility differently.