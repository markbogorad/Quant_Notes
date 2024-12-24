up:: [[Derivatives MOC]]
tags:: #Finance 
# Speed
$$\text{Speed} = \frac{\partial \Gamma}{\partial S}\hspace{1cm}\text{OR}\hspace{1cm}\text{Speed} = \frac{\partial \Gamma}{\partial S} = \frac{\partial^3 V}{\partial S^3}$$
- 1st formula -> traditional speed
- 2nd formula -> speed defined by Wilmott
- **Speed is the rate of change of [[Gamma]] with respect to stock price**
	- Used to estimate *by how much* will traders need to rehedge per 1$ move in the underlying

>"Traders use the gamma to estimate how much they will have to rehedge by if the stock moves. The stock moves by $1 so the [[Delta]] changes by whatever the [[Gamma]] is. But that’s only an approximation. The delta may change by more or less than this, especially if the stock moves by a larger amount, or the option is close to the strike and expiration. Hence the use of speed in a higher-order [[Taylor Series]] expansion." - Wilmott