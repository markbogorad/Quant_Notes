up:: [[Calculus MOC]]
tags:: #Math
# Total Derivatives
- A multivariable calculus concept
- The rate of change of f with respect to 2 (or more?) variables (x, y)
- Key difference between [[Partial Derivatives]]: total derivatives *take into account both variables at the same time* and the variables may also be a function of each other as seen in [[Implicit Differentiation]]
- The total derivative gives you a formula that describes how the output of a function changes as the primary independent variable changes, considering all indirect effects through other dependent variables. 
	- For example, if $z=f(x,y)$ and both $x$ and $y$ are functions of $t$, the total derivative $dtdz$​ would consider how $z$ changes directly with $t$ through $x$ and $y$.
## Mathematically:
- For a function $f(x,y)$, the total differential **$df$ is given by $df = f_x \, dx + f_y \, dy$**
	- Where $f_x$ and $f_y$ are [[Partial Derivatives]] of f with respect to x and y respectively
- Total differential
	- $df=f_x​dx+f_y​dy$
	- **Solving:**
		- Take partial derivative of each and add them together (also multiplying each by $dx$ and $dy$ where necessary)
## 2nd Order Total Derivative
- $d^2 f = f_{xx} \, (dx)^2 + 2 f_{xy} \, dx \, dy + f_{yy} \, (dy)^2$
	- where
		- $f_{xx} \, (dx)^2$ : Represents the second-order change due to x .
		- $f_{yy} \, (dy)^2$ : Represents the second-order change due to y.
		- $2 f_{xy} \, dx \, dy$ :Represents the cross term due to the interaction between changes in \( x \) and \( y \). The factor of 2 arises because the mixed derivative $f_{xy}$ appears twice in the expansion.
- **Second-Order Partial Derivatives:**
	   - $f_{xx} = \frac{\partial^2 f}{\partial x^2}$
		   - The second partial derivative of \( f \) with respect to \( x \). This measures how \( f_x \) changes as \( x \) changes.
	   - $f_{yy} = \frac{\partial^2 f}{\partial y^2}$
		   - The second partial derivative of \( f \) with respect to \( y \). This measures how \( f_y \) changes as \( y \) changes.
	   - $f_{xy} = f_{yx} = \frac{\partial^2 f}{\partial x \partial y}$
		   - The mixed partial derivative, which measures how $f_x$ changes as $y$ changes (or equivalently, how $f_y$ changes as $x$ changes).
### Connection to [[Taylor Series]]
**Taylor Series Expansion:**
   - The second-order total differential can be derived from a second-order Taylor series expansion of the function $f$ around a point $(x_0, y_0)$
   -    $f(x_0 + dx, y_0 + dy) \approx f(x_0, y_0) + f_x \, dx + f_y \, dy + \frac{1}{2} \left( f_{xx} \, (dx)^2 + 2 f_{xy} \, dx \, dy + f_{yy} \, (dy)^2 \right)$
	   - The terms in the expansion involving $(dx)^2$, $( (dy)^2)$, and $( dx \, dy)$ are the second-order differentials.

- **Consideration of All Changes:**
   The second-order total differential captures not only the primary rates of change (first-order partial derivatives) but also how these rates themselves change (second-order partial derivatives). It accounts for *the curvature of the function in both the \( x \)- and \( y \)-directions, as well as the interaction between changes in \( x \) and \( y \).*

