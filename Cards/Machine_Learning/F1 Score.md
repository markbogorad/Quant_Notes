up:: [[Supervised Learning MOC]]
tags:: #Machine_Learning
# F1 Score
$$\text{F1} = 2* \frac{precision*recall}{precision+recall}$$
- Precision
	- measures the proportion of correctly predicted positive observations out of all observations predicted as positive
	- = True positives / true positives + false positives
	- *"Of all the predicted positive instances, how many are actually correct?"*
- Recall
	- measures the proportion of correctly predicted positive observations out of all actual positive observations
	- = true positives / true positives + false negatives
	- *"Of all the actual positive instances, how many did the model correctly identify?"*
- Harmonic mean of the precision and recall
- Lies between $[0, 1]$
- Shows how precise (how many instances correctly classified) and robust (it did not misclassify a significant number of instances) the model is
    - High precision + low recall → high accuracy
        - Large number of difficult instances missed
    - Higher F1 score → better performing model
        - Trying to balance the two.

## Types of positives and negatives
- True positive: correctly predicting positive class
- True negative: correctly predicting negative class
- False positive: incorrectly predicting positive class (Type I error)
- False negative: incorrectly predicting negative class (Type II error)