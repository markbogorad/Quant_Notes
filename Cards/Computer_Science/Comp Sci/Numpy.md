up:: [[Python MOC]]
tags:: #Programming 
# Numpy
- A library for numerical computation
- [[Pandas]] is more like spreadsheets, numpy arrays are more like [[Matrices]]
	- A complement to Pandas
### Key Features of NumPy
1. **N-Dimensional Array Object (`ndarray`):**
   - The core feature of NumPy is its powerful N-dimensional array object, `ndarray`, which can represent vectors, matrices, or higher-dimensional data.
   - `ndarray` allows you to perform fast element-wise operations, broadcasting, and slicing, similar to operations on standard Python lists but with significantly better performance and efficiency.

2. **Vectorized Operations:**
   - NumPy enables you to perform operations on entire arrays without the need for explicit loops, which is known as vectorization. This makes code faster and more concise.
   - For example, you can add two arrays together with `a + b`, rather than using a loop to add corresponding elements.

3. **Broadcasting:**
   - Broadcasting allows NumPy to perform arithmetic operations on arrays of different shapes by automatically expanding the smaller array to match the shape of the larger one.
   - This feature simplifies code by eliminating the need for manual replication of arrays.

4. **Mathematical Functions:**
   - NumPy provides a wide range of mathematical functions, including trigonometric, statistical, and algebraic functions, that can be applied to arrays.
   - Functions like `np.mean()`, `np.std()`, `np.sum()`, `np.dot()` (for dot products), `np.linalg.inv()` (for matrix inversion), and many others are essential for numerical computing.

5. **Linear Algebra:**
   - NumPy has a dedicated submodule, `numpy.linalg`, for linear algebra operations, including matrix multiplication, eigenvalue computation, matrix decomposition, and more.
   - It supports operations like matrix inversion, determinant calculation, solving linear systems, and singular value decomposition (SVD).

6. **Random Number Generation:**
   - NumPy's `random` module provides tools for generating random numbers, creating random samples, and performing random operations like shuffling.
   - It supports various distributions (e.g., normal, binomial, uniform) for generating random numbers for simulations or randomized algorithms.

7. **Array Manipulation:**
   - NumPy offers extensive functions for reshaping, joining, splitting, and modifying arrays. For example, you can reshape an array with `np.reshape()`, concatenate arrays with `np.concatenate()`, or split arrays with `np.split()`.

8. **Efficient Memory Usage:**
   - NumPy arrays use a contiguous block of memory, which ensures efficient access and processing. This is a key reason why NumPy operations are much faster than equivalent operations in standard Python lists.
   - NumPy also allows specifying the data type (`dtype`) of the array elements, enabling further memory optimization.

9. **Interoperability with Other Libraries:**
   - NumPy arrays are the foundation for many other libraries in Python, such as Pandas (for data manipulation), SciPy (for scientific computing), and Matplotlib (for plotting).
   - NumPy arrays can be easily converted to and from other data structures like Pandas DataFrames or even native Python lists.

10. **File I/O:**
    - NumPy provides functions for reading and writing data to and from files. You can save arrays to disk with `np.save()` and load them with `np.load()`.
    - It also supports reading from and writing to text files, including CSV files, with functions like `np.genfromtxt()` and `np.savetxt()`.

11. **Integration with C/C++ and Fortran:**
    - NumPy allows you to integrate code written in C, C++, or Fortran, which can be crucial for optimizing performance in computationally intensive tasks.
    - This makes NumPy not only a high-level tool but also a bridge to lower-level, performance-critical code.

12. **Broadcasting Rules:**
    - Broadcasting in NumPy follows specific rules that make it possible to perform operations on arrays with different shapes in a manner that is intuitive and efficient.