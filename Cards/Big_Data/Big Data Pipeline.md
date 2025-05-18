up:: [[Data MOC]]
tags:: #Programming 
# Big Data Pipeline
1. **You launch an EC2 instance** → like a remote computer.
2. **You install Docker**, and use it to run **Hortonworks Sandbox**.
3. **Inside the Sandbox is HDP 2.6.5**, which includes Hadoop + Hive + Ambari.
4. You **upload data to HDFS**, query it with **Hive (via Ambari or Hue)**.
5. You can **access this data from Python** using **ODBC + pyodbc**.
## Infrastructure & Virtualization

| Component   | What It Is                     | Role                                                                             |
| ----------- | ------------------------------ | -------------------------------------------------------------------------------- |
| [[AWS EC2]] | Cloud virtual machine from AWS | Provides the **hardware** (compute & memory) on which everything else runs.      |
| [[Docker]]  | Containerization platform      | Runs **Hortonworks Sandbox** and related services in isolated containers on EC2. |

### Big Data Platform Layer

| Component                                 | What It Is                                        | Role                                                                                              |
| ----------------------------------------- | ------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| [[Hadoop (Apache)]]                       | Open-source big data framework                    | Provides the **distributed storage (HDFS)** and **processing engine (MapReduce)** for large data. |
| **Apache**                                | Software foundation                               | Maintains Hadoop and related tools like Hive, Pig, etc.                                           |
| **Cloudera**                              | Big data software company                         | Merged with Hortonworks; offers enterprise Hadoop solutions.                                      |
| [[Hortonworks (Cloudera) Sandbox]]        | (Now part of Cloudera)                            | Developed Hadoop distributions (like HDP) tailored for enterprise use.                            |
| **Hortonworks Sandbox**                   | Pre-configured virtual environment by Hortonworks | Contains Hadoop + tools like Hive, Pig, Ambari etc., for **learning and prototyping**.            |
| **HDP 2.6.5** (Hortonworks Data Platform) | Specific version of the Hadoop ecosystem          | Contains versions of Hadoop, Hive, Pig, Ambari etc., bundled together. Used inside Sandbox.       |

---

### Cluster Management & Interface

|Component|What It Is|Role|
|---|---|---|
|**Ambari**|Web-based management interface (from Hortonworks)|Used to monitor, start/stop, and manage Hadoop services in HDP.|
|**Hue**|Web UI for Hadoop services|Provides a user-friendly **interface to run queries**, browse HDFS, manage Hive tables, etc.|

---

### Data Layer & Query Engine

| Component                | What It Is            | Role                                                                                          |
| ------------------------ | --------------------- | --------------------------------------------------------------------------------------------- |
| [[Hive]]                 | SQL engine for Hadoop | Lets you run SQL-like queries on big data stored in Hadoop (on HDFS).                         |
| [[OBDC Driver + pyodbc]] | Connector software    | Lets **external programs like Excel, Python, etc. connect** to Hive over ODBC.                |
| **pyodbc**               | Python package        | Used in Python to connect to databases (like Hive) via ODBC, enabling Python-based analytics. |

---



    
