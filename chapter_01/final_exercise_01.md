# Final Exercise 01 - Introduction to Hadoop Ecosystem - Q&A :question:
## Goals:
- Facilitate a comprehensive understanding of the Hadoop ecosystem among the new team members.
- Guide them in connecting theoretical concepts with real-world applications and use cases.
- Encourage inquisitive thinking and the development of problem-solving skills related to big data processing.
- Assist the newbies in navigating through complex topics and clarifying doubts.
- Foster an environment where team members feel comfortable asking questions and seeking clarifications.
- Assess the understanding and grasp of concepts by the newbies through their responses and discussions.

:warning: **Note:**
- Be prepared to provide detailed explanations and practical examples for each concept.
- Encourage open-ended discussions and critical thinking rather than just focusing on right or wrong answers.
- Provide feedback on their responses, highlighting areas of strength and suggesting improvements where necessary.
- Be approachable and patient, understanding that each team member may have a different pace and style of learning.

### Mentor-Led Q&A and Discussion
**Est. Time:** 3 hours
- Lead an open forum for questions, clarifications, and in-depth discussions.
- Guide discussions towards practical implications and real-world applications of Hadoop ecosystem components.
- Share experiences and insights from your own professional journey to give context to the learnings.

### Role in Facilitating Discussion for Each Chapter

**Chapters 1-5:**
- Focus on the fundamental concepts of Hadoop, HDFS, MapReduce, YARN, and Hive.
- Encourage understanding of the architecture and its impact on big data processing.

**Chapters 6-8:**
- Discuss the importance of ZooKeeper, HBase, and Kafka in distributed systems.
- Illustrate with examples how these components interact within the Hadoop ecosystem.

**Chapters 10-11:**
- Explain Impala's significance in the ecosystem, emphasizing on query execution and partitioning.
- Explore real-world scenarios where Impala and partitioning strategies optimize data processing.

**Chapter 12:**
- Dive deep into the security aspects of big data with Kerberos authentication.
- Discuss practical scenarios where Kerberos is essential for secure data handling.

**Chapter 13:**
- Elucidate the role of Oozie in job scheduling and workflow management.
- Encourage discussions on the practicalities of implementing Oozie in a Hadoop environment.

### Wrapping Up the Session

- Conclude with a recap of key points discussed during the session.
- Provide guidance on further resources or areas of study for the team members.
- Encourage them to apply these learnings to upcoming projects or tasks.

As a mentor, your goal is to ensure that by the end of this session, each team member has a solid foundational understanding of the Hadoop ecosystem, feels confident in their knowledge, and is inspired to continue learning and exploring the field of big data.

## Answers

### Chapter 1: Introduction to Big Data and Hadoop

1. **Q:** What is Apache Hadoop?  
   **A:** Apache Hadoop is an open-source software framework used for distributed storage and processing of large datasets using the MapReduce programming model.

2. **Q:** Can you name a few vendor-specific distributions of Hadoop?  
   **A:** Yes, some vendor-specific distributions of Hadoop include Cloudera, Amazon EMR, and Microsoft Azure.

3. **Q:** What are the three modes in which Hadoop can run?  
   **A:** Hadoop can run in three modes: Standalone mode, Pseudo-distributed mode, and Fully-distributed mode.

4. **Q:** What is the primary role of the `hadoop-env.sh` configuration file?  
   **A:** The `hadoop-env.sh` file is used to configure environment variables for Hadoop, such as setting the Java home directory.

5. **Q:** What purpose does the `core-site.xml` file serve?  
   **A:** The `core-site.xml` file configures Hadoop core settings, including I/O settings and the default file system URL.

### Chapter 2: Hadoop Distributed File System (HDFS)

6. **Q:** What is HDFS?  
   **A:** HDFS, or Hadoop Distributed File System, is a distributed file system designed to run on commodity hardware. It is highly fault-tolerant and is designed to be deployed on low-cost hardware.

7. **Q:** What is the role of the NameNode in HDFS?  
   **A:** The NameNode is the master server that manages the file system namespace and regulates access to files by clients. It maintains the file system tree and the metadata for all the files and directories.

8. **Q:** What is a DataNode in HDFS?  
   **A:** A DataNode stores data in the HDFS. It serves read and write requests from the file system's clients and performs block creation, deletion, and replication upon instruction from the NameNode.

9. **Q:** How does HDFS achieve fault tolerance?  
   **A:** HDFS achieves fault tolerance by replicating data blocks across multiple DataNodes in the cluster, ensuring no single point of failure.

10. **Q:** Can you explain rack awareness in HDFS?  
    **A:** Rack awareness is the concept used in HDFS to improve network traffic while reading/writing data and also to improve the fault tolerance. The NameNode chooses DataNodes that are on different racks for data replication to ensure that even if an entire rack fails, the data is safe.

### Chapter 3: MapReduce Programming Model

11. **Q:** What is MapReduce?  
    **A:** MapReduce is a programming model and an associated implementation for processing and generating large datasets with a parallel, distributed algorithm on a cluster.

12. **Q:** What is the role of a Mapper in MapReduce?  
    **A:** A Mapper processes input data and creates key-value pairs for the Reducer to process.

13. **Q:** What is the role of a Reducer in MapReduce?  
    **A:** A Reducer takes the output from a Mapper as input and combines those data tuples into a smaller set of tuples.

14. **Q:** What is meant by "Shuffling" in MapReduce?  
    **A:** Shuffling in MapReduce is the process of transferring data from Mappers to Reducers, typically involving sorting and partitioning.

15. **Q:** Can a MapReduce job have zero Reducers?  
    **A:** Yes, a MapReduce job can have zero Reducers if no reduction is needed, and it is known as a "map-only" job.

### Chapter 4: Hadoop YARN

16. **Q:** What is YARN?  
    **A:** YARN (Yet Another Resource Negotiator) is a resource management layer of Hadoop that allows multiple data processing engines to handle data stored in a single platform, thus enabling resource sharing and cluster utilization.

17. **Q:** What are the main components of YARN?  
    **A:** The main components of YARN include the Resource Manager, Node Manager, Application Master, and Container.

18. **Q:** What is the Resource Manager in YARN?  
    **A:** The Resource Manager is the master service of YARN that manages the allocation of compute resources in the cluster.

19. **Q:** What is the role of the Node Manager in YARN?  
    **A:** The Node Manager is a per-node service that manages the lifecycle of containers on that node and reports the node's resource usage to the Resource Manager.

20. **Q:** How does YARN provide fault tolerance?  
    **A:** YARN provides fault tolerance by restarting failed tasks on different nodes and by storing application progress in a persistent store for recovery.

### Chapter 5: Apache Hive

21. **Q:** What is Apache Hive?  
    **A:** Apache Hive is a data warehouse software project built on top of Apache Hadoop for providing data query and analysis.

22. **Q:** What is the Hive Metastore?  
    **A:** The Hive Metastore is a central repository in Hive that stores metadata for Hive tables, such as the schema and location of data files.

23. **Q:** What is HiveQL?  
    **A:** HiveQL is a SQL-like query language used in Apache Hive for querying data stored in a Hadoop cluster.

24. **Q:** What are partitions in Hive?  
    **A:** Partitions in Hive are a way of dividing a table into different parts based on the values of a particular column to optimize query performance.

25. **Q:** Can you define SerDe in the context of Hive?  
    **A:** SerDe stands for Serializer/Deserializer. It's a component of Hive used to read and write data from tables and convert it into a format suitable for processing.

### Chapter 6: Apache ZooKeeper

26. **Q:** What is Apache ZooKeeper and what role does it play in a distributed environment?
   **A:** Apache ZooKeeper is a centralized service for maintaining configuration information, naming, providing distributed synchronization, and providing group services. It plays a crucial role in a distributed environment by managing and coordinating a large cluster of machines. ZooKeeper's architecture provides high availability and reliability, ensuring that the distributed applications it manages can be robust against failures.

27. **Q:** Can you explain the concept of znodes in ZooKeeper?
   **A:** Znodes are the data nodes in ZooKeeper's data hierarchy. They are similar to files and directories in a standard file system, except that each znode can hold both data and children. Znodes maintain a stat structure, which includes version numbers for data changes, ACL changes, and timestamps, to facilitate cache validation and coordinated updates.

28. **Q:** How does ZooKeeper handle coordination and configuration management across distributed systems?
   **A:** ZooKeeper handles coordination and configuration management by providing a simple and high-performance kernel for building more complex coordination primitives at the client. It maintains a standard hierarchical namespace, similar to a file system, which allows distributed processes to coordinate with each other through ZooKeeper's znodes. Clients can read from and write to these znodes, allowing them to synchronize and manage configuration across the distributed system.

29. **Q:** What are ephemeral nodes and sequence nodes in ZooKeeper, and how are they used?
   **A:** Ephemeral nodes are znodes that exist as long as the session that created them is active. They are used for locks or as markers in a distributed system. If the session ends, the ephemeral nodes are deleted. Sequence nodes, on the other hand, are znodes with a unique monotonically increasing number appended to them. They are typically used for implementing synchronization primitives like locks and queues.

30. **Q:** How does ZooKeeper ensure data consistency and reliability across distributed nodes?
   **A:** ZooKeeper ensures data consistency and reliability by employing a consensus protocol called Zab (ZooKeeper Atomic Broadcast). This protocol ensures that all updates to the system occur in a total order, meaning all clients see the same transaction order. ZooKeeper's service is replicated over a set of hosts (called an ensemble) to avoid a single point of failure. Each time a transaction is performed, it is broadcast and replicated to a majority of the ensemble, ensuring data reliability and consistency across distributed nodes.

### Chapter 7: Apache HBase

31. **Q:** What is Apache HBase?
    **A:** Apache HBase is an open-source, distributed, versioned, non-relational database modeled after Google's Bigtable and is written in Java.

32. **Q:** What is a Row Key in HBase?
      **A:** A Row Key is a unique identifier for each row in an HBase table, determining the physical storage location of the data.

33. **Q:** What is a Column Family in HBase?
    **A:** A Column Family is a collection of columns in an HBase table that are stored together on the disk.

34. **Q:** How does HBase ensure data availability and fault tolerance?
    **A:** HBase ensures data availability and fault tolerance through data replication across different nodes in the cluster and automatic failover capabilities.

35. **Q:** What is the role of ZooKeeper in an HBase environment?
    **A:** ZooKeeper is used in HBase for master election, server lease management, bootstrapping, and coordination between servers.

### Chapter 9: Apache Kafka

36. **Q:** What is Apache Kafka?
    **A:** Apache Kafka is a distributed streaming platform that is used for building real-time data pipelines and streaming applications.

37. **Q:** What are Topics in Kafka?
    **A:** Topics are categories or feed names to which records are published. Topics in Kafka are multi-subscriber; they can be consumed by multiple consumers.

38. **Q:** What are Partitions in Kafka?
    **A:** Partitions are ordered, immutable sequences of records that are continually appended. A topic may have multiple partitions to allow the data to be scaled.

39. **Q:** What is the role of a Broker in Kafka?
    **A:** A Broker is a Kafka server that stores data and serves client requests. Each broker can handle a certain load of data, and together they form the entire Kafka cluster.

40. **Q:** What is the difference between a Kafka Producer and a Consumer?
    **A:** A Kafka Producer is responsible for publishing records to Kafka topics. A Kafka Consumer subscribes to topics and processes the feed of published records.

### Chapter 10: Apache Impala

41. **Q:** What is Apache Impala?
    **A:** Apache Impala is an open-source, massively parallel processing (MPP) SQL query engine for processing and analyzing data stored in Hadoop Distributed File System (HDFS) and HBase.

42. **Q:** What is an Impala Daemon?
    **A:** An Impala Daemon, often referred to as an Impalad, is a process that runs on each node of an Impala cluster. These daemons are responsible for executing queries and processing data in parallel.

43. **Q:** What is the role of a Catalog Service in Impala?
    **A:** The Catalog Service in Impala serves as a centralized metadata repository for the cluster. It stores metadata information about tables, partitions, schemas, and data locations.

44. **Q:** What is the role of a Query Coordinator in Impala?
    **A:** A Query Coordinator in Impala is responsible for managing the overall execution of a query. It coordinates its execution across multiple Impala Daemons and ensures the results are returned to the user or application.

45. **Q:** What is the difference between Refresh and Invalidate in Impala?
    **A:** "Refresh" reloads the metadata for a specific table or partition from the underlying storage system. "Invalidate" invalidates the cached metadata for a specific table or the entire catalog.

### Chapter 11: Partitioning

46. **Q:** What is Partitioning in databases and data storage?
    **A:** Partitioning is the process of dividing a database or its elements into discrete parts to improve manageability, performance, and availability.

47. **Q:** What are some common partitioning criteria?
    **A:** Common partitioning criteria include numerical ranges, alphabetical ranges, hash values, and datetime intervals.

48. **Q:** What is a Partition Key?
    **A:** A Partition Key is a column or a set of columns that determines how the data is partitioned and stored in the database.

49. **Q:** Can you explain Partition Pruning?
    **A:** Partition Pruning is an optimization technique used in query processing where the query optimizer eliminates unnecessary partitions and only scans the relevant ones.

50. **Q:** How is datetime-based partitioning used in real-world scenarios?
    **A:** Datetime-based partitioning is used to organize and manage time-series data efficiently, like financial transactions or event logs, allowing for faster access and analysis of data based on time intervals.

### Chapter 12: Kerberos Authentication

51. **Q:** What is the primary purpose of the Key Distribution Center (KDC) in the Kerberos authentication system, and what are its two main components?  
    **A:** The primary purpose of the Key Distribution Center (KDC) in the Kerberos authentication system is to facilitate secure, authenticated communication between clients and services within a network. The KDC serves as a trusted third party that verifies the identities of clients and services. It has two main components:
      - **Authentication Server (AS):** Responsible for verifying the identity of users and issuing Ticket Granting Tickets (TGTs).
      - **Ticket Granting Server (TGS):** Uses the TGT to issue service tickets, which clients use to access various network services securely.
    
52. **Q:** How does the "kinit" command contribute to the Kerberos authentication process, and what does it allow users to obtain?  
    **A:** The "kinit" command initiates the Kerberos authentication process for a user. It allows users to request and obtain a Ticket Granting Ticket (TGT) from the Kerberos Key Distribution Center (KDC). The TGT is then used to request service tickets for accessing specific network services, ensuring that the user doesn't need to repeatedly enter their credentials.

53. **Q:** Explain the concept of "Single Sign-On (SSO)" in the context of Kerberos authentication and its benefits for users.  
    **A:** Single Sign-On (SSO) in the context of Kerberos authentication is a feature that allows users to authenticate once and gain access to multiple services without re-entering their credentials. The benefits include:
      - **Convenience:** Users only need to remember and provide their credentials once during the login session.
      - **Reduced Administrative Overhead:** Fewer password resets and user account management.
      - **Enhanced Security:** Limits the exposure of user credentials and reduces the chances of credential theft.
      - **Streamlined User Experience:** Users can seamlessly access multiple services without interruption.
    
54. **Q:** Why is the concept of "time sensitivity" important in Kerberos authentication, and how does it enhance security?  
    **A:** Time sensitivity in Kerberos authentication refers to the use of timestamps and time-limited tickets. It enhances security by:
      - **Preventing Replay Attacks:** Ensuring that old authentication messages cannot be reused by attackers.
      - **Limiting Ticket Validity:** Tickets have a limited lifetime, reducing the window of opportunity for unauthorized use if a ticket is compromised.
      - **Synchronizing Clocks:** Minimizing the discrepancies between the clocks of different network components to prevent unauthorized access due to time mismatches.
    
55. **Q:** In what real-world scenarios or use cases is Kerberos authentication commonly employed, and how does it contribute to security and ease of use in those contexts?  
    **A:** Kerberos authentication is commonly employed in:
      - **Enterprise Environments:** For securing access to sensitive corporate resources, ensuring that only authorized personnel can access critical systems.
      - **Online Banking and E-commerce:** To protect user transactions and personal data.
      - **Government and Military Communication Systems:** To secure communication channels and data access.
      - **Cloud Services:** To provide secure access and data protection in cloud environments.
    In these scenarios, Kerberos enhances security through robust authentication mechanisms while providing a seamless and efficient user experience with Single Sign-On capabilities.

### Chapter 12: Oozie Workflow Scheduler

56. **Q:** What is Apache Oozie, and how does it facilitate job scheduling and workflow management in a Hadoop environment?
    **A:** Apache Oozie is a server-based workflow scheduling system to manage Hadoop jobs, facilitating job scheduling by defining complex, multi-stage workflows in XML and managing their execution.

57. **Q:** Can you differentiate between an Oozie Workflow job and a Coordinator job?
    **A:** A Workflow job is a sequence of actions to accomplish a specific data processing task. A Coordinator job schedules Workflow jobs based on time or data availability.

58. **Q:** Describe the lifecycle of an Oozie job.
    **A:** An Oozie job lifecycle includes states like PREP (being set up), RUNNING (in progress), SUCCEEDED (completed successfully), KILLED (terminated before completion), and FAILED (failed to complete successfully).

59. **Q:** How does Oozie support SLA (Service Level Agreement) monitoring?
    **A:** Oozie supports SLA monitoring by allowing users to specify time-based criteria for job completion and set up notifications for when these criteria are not met, ensuring timely data processing.

60. **Q:** What are the main components of an Oozie Workflow job?
    **A:** The main components include Control Nodes (define the flow of the job), Action Nodes (represent the tasks), workflow.xml (defines the Workflow job), and job.properties (contains properties required by the workflow.xml).
