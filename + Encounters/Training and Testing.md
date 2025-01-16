up:: [[Supervised Learning MOC]]
tags:: #Machine_Learning 
# Train-Test Split
- Train
	- `fit` in sklearn in [[Python MOC]]
	- `lr.fit(X_train, y_train)` where lr is an instance of the model, for example `lr=LinearRegression()`
		- fit method uses least square loss automatically ([[OLS Estimator]])
		- X train is going to be a huge matrix of features
		- Y train is going to be your dependent variable
- Test
	- Usually 20% of the data
	- `predict` in sklearn
	- `predictions_train = lr.predict(X_train)`
		- See the fit on training data
	- `predictions_test = lr.predict(X_test)`
		- See the fit on testing data
		- Compare using `metrics.r2_score()` from sklearn
- Shuffling
	- Set to true by default, set to false when time dependent
	- Shuffle for cross sectional data -> order will not contain special information
		- [[Time Series, Cross Sectional, Panel Data]]
			- shuffle=true -> cross sectional
			- shuffle=false -> time series
