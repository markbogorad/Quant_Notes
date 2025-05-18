up:: [[Supervised Learning MOC]], [[Deep Learning MOC]]
tags:: #Machine_Learning 
# Machine Learning Notation

|**Notation**|**Name**|**Definition / Meaning**|**Common Usage**|**Example**|
|---|---|---|---|---|
|arg⁡max⁡xf(x)|Argmax|Returns the value of x that **maximizes** f(x)|Classification (e.g., pick the class with highest score)|arg⁡max⁡x∈{1,2,3}(2x−x2)=1|
|arg⁡min⁡xf(x)|Argmin|Returns the value of x that **minimizes** f(x)|Loss minimization, model fitting|arg⁡min⁡x(x2+4x+5)=−2|
|∥x∥|Norm (L2 by default)|Vector magnitude. Default is L2 norm x12+⋯+xn2|Regularization (Ridge), distance metrics|∥[3,4]∥=5|
|∥x∥1|L1 Norm|Sum of absolute values of a vector: (|x_1|+|
|∥x∥0|L0 “Norm”|Count of non-zero elements in x (not a true norm)|Feature selection, sparsity|∥[0,1,3]∥0=2|
|∇f(x)|Gradient|Vector of first-order derivatives of f with respect to x|Optimization, gradient descent|∇f(x,y)=[∂f/∂x,∂f/∂y]|
|σ(x)|Sigmoid function|Logistic function: 11+e−x, output in range (0, 1)|Binary classification, neural nets|σ(0)=0.5, σ(2)≈0.88|
|1{A}|Indicator function|1 if event A is true, else 0|Accuracy, loss calculation|1{y=y^}|

## Norm
- As layers increase varinace increases
- Power of NNs comes from non linearity
- When inputs of sigmoid of have high variance a lot of the inputs are in the tailed regions
	- The gradeints of those regions are 0 so if theres too much mass there you can't learn