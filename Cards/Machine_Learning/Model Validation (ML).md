up:: [[Machine Learning Miscellaneous MOC]]
tags:: #Programming 
# Model Validation
- Where trained model is evaluated against validation and testing data
- ![[Pasted image 20240829220923.png]]
1. The first step is to **train** a model and select the hyperparameters using a **validation set**.
2. The second step is to use the best hyperparameters to **retrain** on the **train and validation data.**
3. After you have the fully trained model you **test** the performance against the **test dataset**.
4. If the results are good you can **retrain** the model on all the data to get it **production** ready.

>A rule of thumb is to use 60%, 20%, and 20% respectively for train, validation and test sets.
## Training
- It is the set of data that is used to train and make the model learn the hidden features/patterns in the data, for certain models the same training data is fed into the data repeatedly as the model continues to learn the features of the data.
- You want a lot of data in your training set so that you can have the best learning results.
## Validation
- The validation set is a set of data, separate from the training set, that is used to validate our tentative model performance during training. This validation process gives information that helps us tune the model’s hyperparameters and configurations accordingly.
## Testing
- The test set is a separate set of data used to test the model after completing the training. It provides an unbiased final model performance metric in terms of accuracy, precision, etc. To put it simply, it answers the question of "How well does the model perform?"
- You want a lot of data in the test set so that you can get the best model validation result
## Production
- These sets do not continue any new data, it’s simply combinations of the previous models that we use in later steps to ensure that we use as much data is possible to learn the appropriate model. We can generally ignore the production step, unless we have to put a model into production.

## [[Cross Validation]]
- Deciding how to allocate training vs testing data