up:: [[Machine Learning Miscellaneous MOC]]
tags:: #Programming 
# Supervised Learning Models
## Validation vs Test Data
- Intermediary step between validation and testing
- Validation data
	- What we train the model on
- Test data
	- What is then used for out of sample performance metrics
- **Important rule**
	- 50% of ML papers make this mistake
		- They train their data on the full sample, not strictly the training data
			- This is cheating, as the model sees the entire dataset
## General Rules of Thumb
- GLM (general linear models) perform best on smaller sized datasets and performs well on noisy datasets, provided that certain statistical assumptions are met.
	- [[Multiple Linear Regression]]
- Boosting and bagging algorithms (e.g. random forest and xgboost) perform best on larger tabular datasets, and do not make many statistical assumptions.
	- [[Random Forests]]
	- [[XGBoost]]
- Deep neural networks perform best on very large datasets, preferably on non-tabular datasets (e.g. tensors, pictures, audio, computer vision, text/nlp).
	- [[Neural Networks]]
- In practice we might use linear regression models for ultimate explainability especially if you can specify the important interaction effects; When you only have a few features, you would use explainable boosting machines. You would use extreme gradient boosting, when you have large datasets with many features and unknown interaction effects. You would use probabilistic models when you care about uncertainty estimates, you would use stacked models when you only care about predictive performance, you would use deep learning when you are working with large unstructured datasets.
- ![[Pasted image 20240822100430.png]]