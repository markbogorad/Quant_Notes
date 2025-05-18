up:: [[Numerical Methods MOC]]
tags:: #Math
# Multi-Step Methods
- A generalization of the [[2nd Order Runge-Kutta (Midpoint Method)]]
- Incorporates information from previous steps
$$x_{n+1} = a_0 x_n + a_1 x_{n-1} + a_2 x_{n-2} + \dots + h \left[ b_0 f(x_n, t_n) + b_1 f(x_{n-1}, t_{n-1}) + \dots \right]$$
- $( x_n, x_{n-1}, x_{n-2}, \dots)$ are previous approximations. 
- $( f(x_n, t_n), f(x_{n-1}, t_{n-1}))$ are function evaluations at previous points. 
- $( a_0, a_1, a_2, \dots )$ and $( b_0, b_1, \dots )$ are weights chosen to achieve a desired level of accuracy. 
### Pros
- **Higher Accuracy**: Since more past values are used, higher-order accuracy can be achieved without drastically reducing the step size.
- **Efficiency**: Computing function derivatives (evaluating f(x,t)f(x,t)) is computationally expensive. Instead of re-evaluating derivatives at every step (as in Runge-Kutta methods), multi-step methods reuse previous function values.
- **Stability**: Some problems, especially stiff ODEs, require stable methods that can handle large step sizes without becoming unstable.
### Example of Multi Step Methods
- [[Adams-Bashforth Methods (Explicit)]]
- [[Adams-Moulton Methods (Implicit)]]
