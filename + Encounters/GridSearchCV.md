up:: [[Supervised Learning MOC]]
tags:: #Machine_Learning 
# Grid Search Cross Validation
- A type of [[Cross Validation]] used to tune [[Hyperparameters]] automatically
	- Exhaustively searches over a pre-defined grid of hyperparameters, evaluating all possible combos of hyperparameters and and then doing cross validation
- Example of a parameter grid (for a [[Decision Trees]])
	- `param_grid = { 'max_depth': [3, 5, 10], 
	- `'min_samples_split': [2, 5, 10], `
	- `'criterion': ['gini', 'entropy'] }`
	- Will cross check all these combinations
- Usually the better option for mid to comlpex models, but prone to [[The Curse of Dimensionality]]
### Key Arguments in GridSearchCV
1. **`estimator`**:
    - The machine learning model to tune (e.g., `DecisionTreeClassifier`).
2. **`param_grid`**:
    - Dictionary defining the hyperparameter space (keys are hyperparameter names, values are lists of values to test).
3. **`cv`**:
    - Number of folds for cross-validation (default is 5).
4. **`scoring`**:
    - Metric to optimize (e.g., `'accuracy'`, `'neg_mean_squared_error'`).
