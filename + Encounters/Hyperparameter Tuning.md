up:: [[Machine Learning Miscellaneous MOC]]
tags:: #Programming 
# Hyperparameters
- Parameters set before the learning process begins that control the behavior of the training algorithm
- Ex: number of nodes/layers in a neural network, learning rate, number of epochs

## Hyperparameter Tuning
- The process of finding the optimal hyper parameters
- **Grid Search:** An exhaustive search over a manually specified subset of the hyper parameter space.
- **Random Search:** Randomly sampling hyper parameters from a specified range, which can be more efficient than grid search for some problems.
- **Bayesian Optimization:** A more sophisticated method that models the performance of hyper parameters using a probabilistic model and optimizes over it to find the best set.
- [[Cross Validation]]: Often combined with the above methods to evaluate the performance of different hyper parameter settings and select the one that gives the best generalization performance.

