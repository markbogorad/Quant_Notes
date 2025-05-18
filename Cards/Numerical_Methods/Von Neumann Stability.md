up:: [[Numerical Methods MOC]]
tags:: #Math 
# Von Neumann Stability
- Von Neumann Stability Analysis is a method used in numerical analysis to determine whether a finite difference scheme for solving partial differential equations (PDEs) will remain stable as it progresses in time.
- The method assumes the error can be written as a [[Fourier Transforms]] series and examines how the amplitude of each Fourier mode changes over time.

1. **Assume a solution of the form**:
    
    $u_i^n=G^ne^{ikx_i}$
    
    Where:
    - $u_i^n$​ is the solution at grid point $x_i​$ and time step n.
    - G is the **amplification factor** (how much the error grows or shrinks at each step).
    - k is the **wave number** from the Fourier expansion.
    
2. **Amplification Factor** G:  
    The key to von Neumann stability is analyzing the **growth of GG**.  
    For stability, we require: $∣G∣≤1$
    
    This ensures that errors do not grow over time.