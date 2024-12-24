up:: [[Machine Learning Miscellaneous MOC]]
tags:: #Programming 
# Cross Validation
- How to allocate between training and testing data
- It is a resampling method that uses different portions of the data to test and train a model on different iterations.
### **Types of Cross Validation**
1. **K-fold** → divide into $k$ equal bins, use $k-1$ folds for training, $1$ for testing repeated $k$ times.
2. **Stratified** → ensure each fold has an equal proportion of observations from a given class.
3. **Leave One Out** → leave one instance out of the dataset ($n-1$ for training) repeated $\times n$
4. There are **many variations**, especially when it comes to time series, we will look at these in the future.