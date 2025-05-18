up:: [[Numerical Methods MOC]]
tags:: #Math 
# Discrete Fourier Transforms (DFT)
- The Discrete Fourier Transform (DFT) is used when dealing with finite, discrete data, such as financial time series, option pricing models, and digital signal processing. Since real-world data is usually sampled at discrete points, the DFT is the practical alternative to the continuous Fourier Transform (FT).
$$F(k) = \sum_{n=0}^{N-1} f(n) e^{-i \frac{2\pi}{N} kn}$$
- Inverse:
$$f(n) = \frac{1}{N} \sum_{k=0}^{N-1} F(k) e^{i \frac{2\pi}{N} kn}$$
