up:: [[Supervised Learning MOC]]
tags:: #Machine_Learning 
# Cross Validation
- Checking model performance more than once
- General way it works:
	- Iterative loop where each iteration is a **fold** and each fold checks model performance from a piece of the training data known as the **validation set**
		- 5 folds would make each validation set 20% of the training data
		- Test data is never touched, we only use different pieces of training data
		- The score (whatever loss metric) is calculated at each fold and then averaged
- It is a resampling method that uses different portions of the data to test and train a model on different iterations.
- Only works for cross sectional data [[Time Series, Cross Sectional, Panel Data]]

![[Screenshot 2024-12-30 at 10.27.02 AM.png]]
### **Types of Cross Validation**
1. **K-fold** → divide into $k$ equal bins, use $k-1$ folds for training, $1$ for testing repeated $k$ times.
2. **Stratified** → ensure each fold has an equal proportion of observations from a given class.
3. **Leave One Out** → leave one instance out of the dataset ($n-1$ for training) repeated $\times n$
4. There are **many variations**, especially when it comes to time series, we will look at these in the future.

## In SKlearn
- [[Python MOC]]
- Can set `shuffle=true` and `test_size=.2`
- Full line would be: `X_train, y_train, y_test, = train_test_split(X, y, random_state=42, test_size=0.2, shuffle=True)`

## Training Vs Validation Error
| **Training vs. Validation Error** | **Underfitting**                | **Overfitting**                                | **Unknown Fit**                     | **Good Fit**                                         |
|-----------------------------------|----------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------------------|
| **Validation Error**              | High                            | High                                          | Low                                  | Low (slightly higher than training error)           |
| **Training Error**                | High                            | Low                                           | High                                 | Low                                                 |
| **Bias**                          | High                            | Low                                           | Balanced                             | Balanced                                            |
| **Variance**                      | Low                             | High (or highly sensitive to random outliers) | Balanced                             | Balanced                                            |
