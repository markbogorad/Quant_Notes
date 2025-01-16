up:: [[Supervised Learning MOC]]
tags:: #Machine_Learning 
# Min-Max Scaling
$$x_{\text{scaled}} = \frac{x - \min(x)}{\max(x) - \min(x)}$$
```
# Min-Max Scaling 
scaler = MinMaxScaler() 
X_scaled = scaler.fit_transform(X)
```

- Scales 0-1
- Subtracts the minimum and divides by range of values (max-min)
