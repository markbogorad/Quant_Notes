up:: [[Data MOC]]
tags:: #Programming 
# Big Data
- Datasets too large for [[Relational Databases]] and traditional methods - need new processing technologies
- Big data 4 Vs that define it
	- Volume, Velocity (how fast you need to store), Variety, Value (how effectively it can be processed for profit)
- Techniques such as massively [[Parallelism C++]] processing and in-memory data storage are generally required, and extremely efficient software coding
- The security requirements of the financial markets, including the need for 24/7 uptime, access controls, audit trails and rollbacks, are beyond many common Big Data technologies, which tend to suffer from their open-source origins and lack enterprise-grade functionality
## Big Data (HDFS) vs [[Relational Databases]]

|Traditional Databases (RDBMS)|Big Data Systems|
|---|---|
|Structured (tables with rows/columns, strict schema)|Unstructured, semi-structured, and structured (text, JSON, logs, audio)|
|Schema-first: You **define the schema**, then insert data|Schema-on-read: You **store data first**, interpret it when you read it|
|Fixed data types, rigid structure|Flexible, can ingest anything|

## Structured vs Unstructured Data
- Structured: data that is formatted into records (pricing updates, trade reports, etc). Typically in [[XML]]
- Unstructured: data with no structure that needs to be parsed, typically with things like [[NLP Natural Language Processing MOC]]
## Main Technologies
- [[Hadoop (Apache)]]
- [[Hortonworks (Cloudera) Sandbox]]
- [[Ambari + Hue]]
- [[Hive]]
- [[OBDC Driver + pyodbc]]
![[Pasted image 20250507113721.png]]