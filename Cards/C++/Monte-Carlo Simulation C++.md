up:: [[C++ MOC]]
tags:: #Programming
# [[Monte-Carlo Simulation]] in C++
## How it looks:
### Simple option valuation [[Structs]]:
- Sets up encapsulated option data + behavior
```
#ifndef OptionData_HPP
#define OptionData_HPP

#include <algorithm> // for max()
using namespace std;  

struct OptionData

// Option data + behaviour
{ 
double K;
double T;
double r;
double sig;

// Extra data
double H; // down and out barrier
double D; // dividend
double betaCEV; // elasticity factor (CEV model)
double scale; // scale factor in CEV model

int type; // 1 == call, -1 == put

double myPayOffFunction(double S)
// Payoff functions
{
// Call option
	if (type == 1)
	{ 
		return max(S - K, 0.0);
	}
	else
	// Put
	{
		return max (K - S, 0.0);
	}
}

};

#endif
```

### Monte-Carlo Test Program
- 3 components:
#### MC Template
```
template <class T> void print(const std::vector<T>& myList)

// A generic print function for vectors:
{ 
std::cout << std::endl << "Size of vector is " << l.size() << "\n[";

// We must use a const iterator here, otherwise we get a compiler error.

std::vector<T>::const_iterator i;

for (i = myList.begin(); i != myList.end(); ++i)

{

std::cout << *i << ",";

  

}


std::cout << "]\n";

}
```
- For templates, see [[Templates C++]]
- 
#### SDE Definition

  
#### Main test
