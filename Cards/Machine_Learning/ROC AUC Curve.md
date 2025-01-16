up:: [[Supervised Learning MOC]]
tags:: #Machine_Learning
# ROC AUC
- The receiver operating curve, also noted ROC, benefit of being independent of the decision threshold (threshold invariant)
- ROC plots the TPR versus FPR by varying the decision threshold for every value from 0%-100%.
- TPR is the **correct positives** over all _positive samples_ and FPR is the **incorrect positives** over all _negatives samples_.
- If the FPR (mistakes on negatives) is smaller that the TPR (success on positives) for all thresholds the model performs better than random.
- The model obtains a perfect score (1 AUC) where no false positive (type 1 errors) or false negatives (type 2 errors) are present for any threshold.
- ROC AUC score is equivalent to calculating the [rank correlation](https://johaupt.github.io/blog/Area_under_ROC_curve.html) between predictions and targets.
- We see that linearly transforming the scores (changing the numbers, but keeping the order the same) does not change the AUC.
- As such AUC is also **scale-invariant**. It measures how well predictions are ranked, rather than their absolute values.
- ROC AUC is the probability that a randomly chosen positive case outranks a randomly chosen negative case based on the classifier (good because positive should be closer to 1).