up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# Multicollinearity
- When you have high correlation among inputs -> basically state a feature twice
- Always plot and examine the inputs matrix
	- `sns.heatmap(X_train.corr())`
- Fix with regularization