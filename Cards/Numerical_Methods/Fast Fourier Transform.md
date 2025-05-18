up:: [[Numerical Methods MOC]]
tags:: #Math 
# Fast Fourier Transform
- Not an equation but an algorithm used to compute [[Discrete Fourier Transform]] faster
- O(Nlogn) speed
- The FFT **recursively breaks down** the DFT computation into smaller DFTs, exploiting symmetry and periodicity to eliminate redundant calculations.
- Used to measure seasonality in [[Time Series]]