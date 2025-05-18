up:: [[Numerical Methods MOC]], [[Numerical Methods MOC]]
tags:: #Math
# ODEs
- *Think of this as the position of something as a function of time*
### Single ODE
An ordinary differential equation (ODE) can be written as:
$$\frac{dx}{dt} = f(x, t)$$
Where:
- $( x(t) )$: The dependent variable, a function of $( t )$ (time or an independent variable).
- $( f(x, t) )$: A function defining the rate of change of $( x(t) )$ with respect to $( t )$.

- **Example:** Population growth or radioactive decay:
	- $\frac{dx}{dt} = r \cdot x$
### System of ODEs
- A system of ODEs consists of multiple interacting equations:
$$\frac{dx_1}{dt} = f_1(x_1, x_2, \dots, x_N, t)$$$$\frac{dx_N}{dt} = f_N(x_1, x_2, \dots, x_N, t)$$
Where:
- Each equation describes how one variable $( x_i(t))$ evolves over time, depending on other variables and $( t )$.

- The system of ODEs can be compactly written in vector form as:
$$\frac{d\mathbf{x}(t)}{dt} = \mathbf{f}(\mathbf{x}, t)$$
Where:
- $( \mathbf{x}(t) = \begin{bmatrix} x_1(t) \\ x_2(t) \\ \vdots \\ x_N(t) \end{bmatrix})$: The vector of dependent variables.
- $( \mathbf{f}(\mathbf{x}, t) = \begin{bmatrix} f_1(x_1, x_2, \dots, x_N, t) \\ f_2(x_1, x_2, \dots, x_N, t) \\ \vdots \\ f_N(x_1, x_2, \dots, x_N, t) \end{bmatrix})$: The vector of functions defining the rates of change.

**Example**: Predator-prey model:
- $\frac{dx_1}{dt} = a x_1 - b x_1 x_2$
- $\frac{dx_2}{dt} = -c x_2 + d x_1 x_2$
