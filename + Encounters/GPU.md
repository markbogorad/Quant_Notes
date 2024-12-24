up:: [[Computer Science MOC]]
tags:: #Programming  
# GPU
![[Pasted image 20240725144808.png]]
- Graphics Processing Unit
	- **Handles heavy computations**
- Used for rendering graphics
- Nvidia makes these
- Its also a [[Semiconductors]]
- Come with huge fans for cooling

## GPU v CPU
- CPU is for HFT
- GPU is for research
- Ex: [[Machine Learning Miscellaneous MOC]]
	- The [[CPU]] might handle data preprocessing and task management
	- The [[GPU]] performs the training of models due to its ability to handle matrix operations and parallel processing efficiently.
- A good CPU and bad GPU
	- Latency will be fast: **CPU is more important for HFT**
	- Good single thread performance, bad [[Multithreading]] performance
	- **Best for:** General-purpose quant finance tasks, such as statistical analysis, financial modeling, and data preprocessing.
	- **Not ideal for**: GPU-accelerated *computations*, *large-scale simulations* that can benefit from parallel processing, and advanced data visualization tasks.
	- Will 
- A bad CPU and good GPU
	- Will have higher latency (bad) and worse data processing
	- Will be able to do [[Monte-Carlo Simulation]] faster (good) and other parallel processing things
	- **Best for:** GPU-intensive tasks like deep learning model training and large-scale parallel simulations.
	- **Not ideal for:** General data analysis, financial modeling, and tasks requiring high CPU performance.
	