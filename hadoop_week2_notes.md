## My Week 2 – Lesson 1 notes:

### Overview of the Hadoop Stack

The Hadoop stack is made up of four main components: 
(1) Hadoop Commons – the libraries and utilities that make everything work, including the libraries for specific applicaitons.
(2) The HDFS (HSDF2 for Hadoop 2.0) – the underlying distributed file storage system for hte instance
(3) Hadoop YARN – the resource (cumpute and storage) allocation systems and schedulers etc.
(4) Hadoop MapReduce - the programming model for large scale processing. Also contains various applications.

### Applications and Frameworks

Applications and frameworks, so HBase is a scalable data warehouse with support for large tables. Hive, a data warehouse infrastructure that provides data summarization and ad hoc querying. 
Pig, which is a high-level data-flow language and execution framework for parallel computation.
Spark, which is a fast and general purpose compute engine which can use the HDFS file system. 
Wide range of applications under Spark, ETL, Machine Learning, stream processing and graph analytics. 

#### Features added into Hadoop2 HDFS

* The cluster resource management and data processing components of MapReduce were separated into two layers MapReduce and YARN. 
* Originally the underlying HDSF consisted of multiple DataNodes; typically one node per cluster, and a single NameNode; the master server that manages the file system namespace and regulates access to "clients". In HDFS2 we now have multiple NameNodes and multiple namespaces.There are also redundant namenodes to ensure higher availability if things fail. 
* HDFS2 also has heterogeneous and archival storage; a mix og SSD, disk, archive etc.
* MaapReduce

#### Namespaces and block IDs

* This can be difficult to get your head around if you're new to Hadoop. This is a really nice introduction to HDSF Federation: http://hortonworks.com/blog/an-introduction-to-hdfs-federation/. It also nicely summarises some of the key benefits.
* HDSF Federation from the Hadoop website:https://hadoop.apache.org/docs/r2.7.2/hadoop-project-dist/hadoop-hdfs/Federation.html

#### YARN

YARN is the next-gen mapreduce. The MapReduce processing from Hadoop 1.0 has been separated our from the cluster management component. Further still YARN separates cluster resource management from job scheduling and monitoring. It has both a Global Manager and separate resource manages for each node. It also has an ApplicationMaster for each application.

#### Apache Tez

Apache Tez provides a developer API and framework to write native YARN applications that bridge the spectrum of interactive and batch workloads. It allows those data access applications to work with petabytes of data over thousands nodes. The Apache Tez component library allows developers to create Hadoop applications that integrate natively with Apache Hadoop YARN and perform well within mixed workload clusters. In this context Apache Tez is run in conjunction (not independentlly) of YARN.

Overview of Apache Tez: http://hortonworks.com/apache/tez/

## My Week 2 – Lesson 2 notes:



