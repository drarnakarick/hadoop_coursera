## My Week 1 – Lesson 1  Notes: ##

### Hadoop Stack Basics: ###

* How does a Hadoop stack work?
* What is the architecture for the framework?
* Apache Hadoop is an open source software framework for storage and large scale processing of datasets on clusters
* Licenced under the Apache Licence
* Created in 2005 — Note: this is around the time I started my first post-doc at LLNL
* Why is it useful? A simple batch processing framework – powerful, quick, and easily scalable.
* Scalibility is at its core. Designed to be cheap and distributed.
* Originally derived from Google’s MapReduce and file ystem.
* Takes a New approach to data: keep all data in the one place, bring compute to the data (don’t move the data!)
* Schema created as the data is read in (efficient)

### The Apache Framework: Basic Modules: ###

* Hadoop Common - contains libraries and utilites needed by other hadoop modules.
* Hadoop Distributed file System (HDFS) - stores data on a distributd machine - with high aggregate badndwith across the cluster
* Hadoop Yarn - resource managemnet platform (schedulign etc)
* Hadoop MapReduce - computing model that scales across different processes

Different applications: Apache PIG (script) , Apache Hive (query), HBase (non-relational data base) can be accessed via MapReduce

NOTE: Hadoop is mainly written in java (with some C and shell scripting on the command line)

### Hadoop Distributed file System (HDFS):###

* Distributed, scalable and portable file-system, written in java to support the Hadoop Framework
* Each HDF stores large files: GBs to TBs and even PBs across multiple machines
* Can achive reliabiltiy by replicating acroos the nodes (doesn’t require raid storage)
* Two nodes: data node &  name node
* Primary and Secondary name nodes (Local and Remote directories)
* Runs on a MapReduce Engine.

Basically involves and SQL store & logs —> ingest service —> CLUSTER —> outgest service  —? SQL store
Consists of a Job tracker and Task Tracker.

MapReduce v2.0 (or MRV2) bacame Hadoop Yarn

Yarn enhances the power of the Hadoop compute cluster: focusses on sheduling. Better calabiliy and improved cluster utilisatio

### Hadoop Zoo:###

Shark (hummingbird), Hadoop (elephant) Jaql, Giraph, Hamma (hippo), Hive (elephant-wasp/bee), Pig & Zoo Keeper

The basic Hadoop Stack includes: Pig & Hive

Application history:

Originally a Google Stack (MapReduce). Added a MySQL gateway for querying; then Sawzall (programming language); Dremel added (metadata manager); Chubby added (system coordination). Facebook, Yahoo and LinkedIn all built on Hadoop Frameworks

Understanding the difference between Hadoop 1.0 and 2.0:

* Hadoop 1.0 had two layers;  MapReduce (cluster resource management & data processing)  & HDFS (redundant, reliable storage)
* Hadoop 2.0 has three layers:  MapReduce (data processing), YARN (cluster resource management) & HDFS (redundant, reliable storage)

You can run existing MapReduce applications (e.g. from Hadoop 1.0) on YARN.


### Hadoop Ecosystem Major Components ( Hadoop Cloudera):###


1. Apache Sqoop: stands for  SQL to Hadoopp. It’s  basically a command line tool designed for efficiently transferring bulk data between Apache Hadoop and structural data stores. It can import individual tables or entire data bases into the HDF system.
2. Hbase: a key component of the Hadoop stack. It based on Google’s big table and it can handle massive datasets (tables) comombinginbillion and billions of rows and millions of columns).
3. PIG: is a scripting langualge, for creating MapReduce programs using Hadoop. The language is called Pig Latin and it excels at describing data analysis problems as data flows. It contains abunch of functions, and allows for use defined funtions. PIG can be just with JRuuby, JPython and Java and you can execute PIG scripts in other languages too.
4. Hive: the software facilitates querying and managing large datasets in the cluster. SQL-like queries can be made using Hive QL.
5. Oozie: ith a worksflow schedule system that manages all the Apache Hadoop jobs.
6. Flume (not the singer): a distributed service for aggregating and move large datasets.

* Additional components: *

1.  Impala: designed specifically for Cloudera. It’s a query engine that runds on top of Apache Hadoop.
2. Spark: a scalable data analytics platform that uses in memory computing – great for supporting machine learning as data can be loaded into the clusters memory and quereyed repeatadly. Spark can interface with HDSF and  Amazon S3

Resources:

Apache Hadoop website:  https://hadoop.apache.org/
An article that nicely explains the various Hadoop components: http://dataconomy.com/hadoop-components-need-know/


Lesson 2: Hands-On Exploration of the Cloudier VM

Quiz #1 Basic Hadoop Stack: 9/10 right.


