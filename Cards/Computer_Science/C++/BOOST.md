up:: [[C++ MOC]]
tags:: #Programming 
# Boost
- Library for enhanced operations [[Libraries]]
## Set Up
- #### Download Boost
	- [Boost C++ Libraries - Browse /boost-binaries at SourceForge.net](https://sourceforge.net/projects/boost/files/boost-binaries/) 
- #### Find the include path
	- In mac terminal: 
		- brew --prefix boost
			- Show location of boost download
				- Location: **/usr/local/opt/boost**
- #### Add path to Boost in "C++ Configurations"
	- ![[Screenshot 2024-03-22 at 1.35.25 PM.png]]
- #### Update `c_cpp_properties.json` include path
	- **Make sure to add "/include" to path name**
```
{
    "configurations": [
        {
            "name": "Mac",
            "includePath": [
                "${workspaceFolder}/**",
                "/usr/local/opt/boost/include", // Adjust this path as necessary
            ],
            "defines": [],
            "macFrameworkPath": [],
            "compilerPath": "/usr/bin/clang++",
            "cStandard": "c11",
            "cppStandard": "c++17",
            "intelliSenseMode": "macos-clang-x64"
        }
    ],
    "version": 4
}
```

- #### Configure CMake
```
cmake_minimum_required(VERSION 3.20)
project(HelloWorld)
set(CMAKE_CXX_STANDARD 20) # Use C++17 or your preferred standard

# Add include directories
include_directories(/usr/local/opt/boost/include)

# Define the source files
set(SOURCES

Shape.cpp
Array.cpp
Circle.cpp
Line.cpp
Point.cpp
main.cpp
)

# Set the output directory for the executable to be the same as CMakeLists.txt
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR})

# Create the executable
add_executable(HelloWorld ${SOURCES})
```

## The Libraries within Boost
- ![[Screenshot 2024-03-24 at 9.19.49 AM.png]]
- ![[Screenshot 2024-03-24 at 9.19.57 AM.png]]

Back:: [[C++ MOC]]
