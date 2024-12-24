up:: [[Machine Learning Miscellaneous MOC]]
tags:: #Programming 
# Overfitting
(1) **If you have large errors on both the training and the validation set, then you have a Bias problem.**

- As such you could select a more complex model or loosen the regularization parameters of the current model.
- You could also develop or select more or better features (columns).
- You could also add more data instances (rows).
- Another option is to train the model for longer, or to stop the model training later.

(2) **If you have small errors on the training set and large errors on the validation set, then you have a Variance problem.**

- The model does not generalize well; one has to reduce the complexity of the model.
- You can also tighten the regularization parameters of the existing model.
- You can perform the appropriate feature selection method to reduce the inputs.
- You could also stop the training early to avoid overfitting.