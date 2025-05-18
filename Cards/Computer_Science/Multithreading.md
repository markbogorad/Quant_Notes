up:: [[Computer Science MOC]], [[Data MOC]]
tags:: #Programming  
# Multithreading
- Running multiple executable paths within one program

|Concept|Key Idea|Simultaneity?|Example Use Case|
|---|---|---|---|
|**Multithreading**|Multiple threads in one process|Not necessarily|UI + background task|
|**Concurrency**|Multiple tasks logically at once|Not necessarily|Database handling many queries|
|**Parallelism**|Multiple tasks physically at once|Yes|MapReduce processing stock data|

- **Multithreading**: One person juggling 3 balls.
- **Concurrency**: One cook making several dishes by switching tasks efficiently.
- **Parallelism**: Several cooks making dishes at the same time in different kitchens.




- Executing multiple threads concurrently within a single process
- By using multiple threads, a program can perform multiple operations at the same time, improving performance and responsiveness.
- On multi-core processors, threads can be executed in parallel, making full use of the [[CPU]] capabilities and improving performance.
- Multithreading can make a program more responsive. For example, in a graphical user interface (GUI) application, one thread can handle user input while another performs background tasks.
- While multithreading can improve performance, it also introduces **overhead**. 
	- Creating and managing multiple threads consumes resources, and improper use can lead to issues like deadlocks, where threads are waiting indefinitely for resources held by each other

## Multithreading in Quant Finance
- High-frequency trading systems require the processing of large volumes of market data and the execution of trades within milliseconds. Multithreading is used to:
- HFT
	- **Process incoming market data feeds** concurrently, ensuring that the system can handle the high data throughput.
	- **Execute trading algorithms** simultaneously, enabling the system to make rapid decisions and place orders quickly.
	- **Handle risk management and compliance checks** in parallel to trading activities to ensure that all trades comply with regulations and risk parameters.
- Data Processing Real Time
	- **Collect and aggregate market data** from various sources concurrently, ensuring up-to-date and accurate data.
	- **Update and display real-time prices, charts, and analytics** in trading platforms, providing traders with the latest information for decision-making.
	- **Run multiple data analysis algorithms** simultaneously to detect patterns, trends, and anomalies in the data.
- Risk
	- **Run multiple simulation paths** in parallel, significantly speeding up the computation time required for risk assessments.
	- **Perform stress testing** on various scenarios concurrently, providing a comprehensive view of potential risks.
	- **Aggregate results and update risk metrics** in real-time, ensuring that risk managers have the latest information.\
- Portfolio Optimization
	- **Evaluate multiple optimization models** concurrently, comparing different strategies to find the best one.
	- **Perform sensitivity analysis** on various parameters in parallel, assessing the impact of changes on the portfolio's performance.
	- **Backtest multiple investment strategies** simultaneously to validate their effectiveness using historical data.
