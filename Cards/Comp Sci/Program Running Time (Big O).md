up:: [[Computer Science MOC]]
tags:: #Programming  
# Running Time
- How quickly a program runs
- Measured with a `O` for upper bound of running time and `Ω` for lower bound

| **Notation**   | **Speed Description**                                                                                                                                                  | **Example**                                                    |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------- |
| **O(1) or**    | **Constant Time**: The running time of the algorithm is constant and does not change with the size of the input.                                                       | Accessing a specific element in an array                       |
| **O(log n)**   | **Logarithmic Time**: The running time grows logarithmically with the input size. Often seen in algorithms that halve the problem size at each step.                   | Binary search in a sorted array ([[Linear Search]])  |
| **O(n)**       | **Linear Time**: The running time grows linearly with the input size.                                                                                                  | Iterating through all elements in a list                       |
| **O(n log n)** | **Linearithmic Time**: The running time grows in a linearithmic manner, which is common in more efficient sorting algorithms.                                          | Merge sort, quicksort (average case) [[Sorting Algorithms]]    |
| **O(n^2)**     | **Quadratic Time**: The running time grows quadratically with the input size. Often seen in algorithms with nested loops.                                              | Bubble sort, selection sort [[Sorting Algorithms]]             |
| **O(n^3)**     | **Cubic Time**: The running time grows cubically with the input size. This is common in algorithms with three nested loops.                                            | Floyd-Warshall algorithm for finding shortest paths in a graph |
| **O(2^n)**     | **Exponential Time**: The running time doubles with each additional element in the input. Typically seen in recursive algorithms that solve subproblems independently. | Recursive solution to the Fibonacci sequence                   |
| **O(n!)**      | **Factorial Time**: The running time grows factorially with the input size. This is often seen in algorithms that generate all permutations of an input set.           | Solving the traveling salesman problem via brute force         |
