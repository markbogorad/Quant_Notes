up:: [[C++ MOC]]
tags:: #Programming
# Inclusion Guards
## How it looks:

```
#ifndef POINT_HPP
#define POINT_HPP

		// Class definition here
		
#endif POINT_HPP
```

- Inclusion guards prevent the HPP file form being included multiple times in the same 
- ifndef
	- if not already defined, define ...

# In [[Templates C++]]:

```
#ifndef POINT_HPP
#define POINT_HPP

		// Class definition here

#indef POINT_CPP
#define POINT_CPP
#endif POINT_CPP

#endif POINT_HPP
```

- In [[Templates C++]], CPP files get linked (Preprocessed) at the bottom of the HPP