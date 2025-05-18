up:: [[Numerical Methods MOC]]
tags:: #Math 
# Stability
- Does the error remain bounded over multiple steps?
- A numerical method is stable if **small errors do not grow uncontrollably** as the solution progresses in time.
- Stability requires that errors in the numerical solution do not **amplify exponentially**:

$$∣x_n−x_{exact,n}∣≤C∣x_0−x_{exact,0}∣$$
- for some constant C independent of n.
- If a method is unstable, small numerical errors get amplified over time, leading to a completely incorrect solution