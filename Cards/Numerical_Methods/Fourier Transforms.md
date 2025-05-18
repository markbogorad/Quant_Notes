up:: [[Numerical Methods MOC]]
tags:: #Math 
# Fourier Transforms
- A tool used to convert a function **from time domain to frequency domain (which frequencies are present in the function)** - decomposition signal into the frequency
- The Fourier Transform breaks the time series into a sum of sinusoidal waves at different frequencies to identify these patterns.
$$f(t)=A0​+A1​cos(2πf1​t)+A2​cos(2πf2​t)+…$$
- Each frequency $f_i$​ tells you **how fast** a pattern repeats, and each amplitude $A_i$​ tells you **how strong** that frequency component is.

- The Fourier Transform doesn’t require the function to look like a wave; it transforms **any function** into a combination of waves (sine and cosine). It answers the question: **"What combination of sine waves could add up to this function?"**
- For example:
	- If you have a time series of daily stock prices, the Fourier Transform tells you which cycles (frequencies) contribute to the movement.
	- You might find that a large part of the series is explained by a low-frequency component (slow-moving trend) and some small high-frequency noise.
- **Fourier Transform Equation:**
$$F(k) = \int_{-\infty}^{\infty} f(x) e^{-i k x} \, dx$$
- **Inverse:**
$$f(x) = \frac{1}{2\pi} \int_{-\infty}^{\infty} F(k) e^{i k x} \, dk$$
	- To reconstruct the original function after analyzing or modifying its frequency components. 
	- In many applications, we transform a function into the frequency domain, make some adjustments, and then transform it back to the time (or spatial) domain using the inverse.
## Numerical Integration with Fourier Transforms
- In practice, you can’t calculate this integral exactly for every function, so you use [[Discrete Fourier Transform]] or [[Fast Fourier Transform]] to approximate it