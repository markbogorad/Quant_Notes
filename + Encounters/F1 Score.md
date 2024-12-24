up:: [[Machine Learning Miscellaneous MOC]]
tags:: #Programming 
# F1 Score
$$\text{F1} = 2 * \frac{1}{\frac{1}{precision} + \frac{1}{recall}}$$
- Harmonic mean of the precision and recall
- Lies between $[0, 1]$
- Shows how precise (how many instances correctly classified) and robust (it did not misclassify a significant number of instances) the model is
    - High precision + low recall → high accuracy
        - Large number of difficult instances missed
    - Higher F1 score → better performing model
        - Trying to balance the two.