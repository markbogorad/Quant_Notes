up:: [[Supervised Learning MOC]]
tags:: #Machine_Learning 
# Scaling
- Transforming the features so they are all on a similar scale or range
	- Helps improve stability, convergence speed, and model performance
- Commonly used transformations
	- Relu (range 0 to infinity)
	- Sigmoid (range 0 to 1)
	- Tanh (range -1 to 1)
### Where scaling is helpful
| **Algorithm**                         | **Features might need scaling?**  |
| ------------------------------------- | --------------------------------- |
| [[SVM]]                               | Yes                               |
| [[K-Nearest Neighbors (KNN)]]         | Yes                               |
| [[Regression]]                        | No (unless regularized, multiple) |
| [[Logistic Regression]]               | No (unless regularized, multiple) |
| Naive Bayes                           | No                                |
| [[Decision Trees]] | No                                |
| [[Random Forests]]               | No                                |
| **AdaBoost**                          | No                                |
| **Neural Networks**                   | Yes                               |

**Note**: Ridge and Lasso regression require scaling of independent variables.
