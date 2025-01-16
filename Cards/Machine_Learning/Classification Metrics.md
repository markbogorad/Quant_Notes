up:: [[Supervised Learning MOC]]
tags:: #Machine_Learning
# Classification Metrics
| Metric              | Formula                                                                           | Interpretation                              | Threshold ≥ 0.5 | Threshold ≥ 0.3 |
| ------------------- | --------------------------------------------------------------------------------- | ------------------------------------------- | --------------- | --------------- |
| Accuracy            | $\frac{\mathrm{TP}+\mathrm{TN}}{\mathrm{TP}+\mathrm{TN}+\mathrm{FP}+\mathrm{FN}}$ | Overall performance of model                | 64%             | 82%             |
| Precision           | $\frac{\mathrm{TP}}{\mathrm{TP}+\mathrm{FP}}$                                     | How accurate the positive predictions are   | 80%             | 86%             |
| Recall, Sensitivity | $\frac{\mathrm{TP}}{\mathrm{TP}+\mathrm{FN}}$                                     | Coverage of actual positive samples         | 57%             | 86%             |
| Specificity         | $\frac{\mathrm{TN}}{\mathrm{TN}+\mathrm{FP}}$                                     | Coverage of actual negative samples         | 75%             | 75%             |
| F1 Score            | $\frac{2 \mathrm{TP}}{2 \mathrm{TP}+\mathrm{FP}+\mathrm{FN}}$                     | Hybrid metric useful for unbalanced classes | 67%             | 86%             |


- Misclassification Error
- Gini Index --> high = bad, low = good
	- Split Quality --> the lower the gini the better the split quality
	- Gini index -> intuition is the probability that the balls have different colors

- Explainability
- Theres a spectrum of interoperable to uninterpertable 
- Local vs global
- visualization metrics vs numerical metrics
- model specific vs model agnostic
- Permutation importance
- When scrambling a features signal causes decline in the models explainability, it means the feature was good
- Shapley Values
- Intuition: looking at how well supporting feature working
	- The way it test --> put in average features instead of good ones and see what has happened

## Regression to Classification Equivalents

|**Regression**|Mean Squared Error|Mean Absolute Error|R-Squared|MAPE|
|---|---|---|---|---|
|**Classification**|Log Loss|Hinge Loss|0-1 Loss|Cross Entropy|