up:: [[Supervised Learning MOC]]
tags:: #Machine_Learning 

| **Metrics**         | **What?**                                                                       | **Why?**                                                 | **When to Use?**                                                    |
|---------------------|---------------------------------------------------------------------------------|----------------------------------------------------------|---------------------------------------------------------------------|
| **MSE**             | Measures average squared difference between estimated and actual values.        | Emphasizes larger errors.                                 | When large errors are more critical.                                |
| **RMSE**            | Square root of MSE, in the same units as the response variable.                 | Easier interpretation of errors.                          | When error scale should match target scale.                         |
| **MAE**             | Average absolute difference between estimated and actual values.                | Less sensitive to outliers.                               | With many outliers or non-normal residuals.                         |
| **MAPE**            | Percentage error between estimated and actual values.                           | Easy interpretation as a percentage.                      | For forecasting and percentage-based error analysis.                |
| **R-Squared**       | Proportion of variance explained by the model.                                  | Indicates model’s explanatory power.                      | To evaluate linear regression models’ fit.                          |
| **Adjusted R-squared** | Statistical measure that modifies the R-Squared value to account for the number of predictors | Unlike R-squared, it penalizes the model for including irrelevant predictors | Useful in multiple regression scenarios where you have several independent variables |
# Mean Squared Error
- average squared difference between the predicted values and the actual values
- used to represent the cost associated with the predictions or the loss incurred in the predictions
- MSE emphasizes larger errors, penalizing models that make significant mistakes more heavily.
- MSE is a continuous and differentiable function, which makes it well-suited for optimization techniques such as [[Gradient Descent]]
- MSE has some limitations, such as its sensitivity to outliers and the absence of an upper bound on its values
$$\text{MSE} = \frac{1}{n} \sum_{i=1}^{n} \left( y_i - \hat{y}_i \right)^2$$

# Root Mean Squared Error
- Square root of MSE
$$\text{RMSE} = \sqrt{\frac{1}{n} \sum_{i=1}^{n} \left( y_i - \hat{y}_i \right)^2}$$
# Mean Absolute Error
- Measures the average magnitude of the errors in a set of predictions, without considering their direction.
- It is the average absolute difference between the predicted and actual values. 
- Unlike MSE, it doesn’t square the errors, which means it doesn’t punish larger errors as harshly
- The absolute value of error is not convenient, because it doesn’t have a continuous derivative, which does not make the function smooth
$$\text{MAE} = \frac{1}{n} \sum_{i=1}^{n} \left| y_i - \hat{y}_i \right|$$
# Mean Absolute Percentage Error
-  expresses the error as a percentage of the actual values, providing an easy-to-understand metric.
- A relative measure of error
$$\text{MAPE} = \frac{1}{n} \sum_{i=1}^{n} \left| \frac{y_i - \hat{y}_i}{y_i} \right| \times 100\%$$
