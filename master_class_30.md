# Google Cloud Platform
## Ismael Yuste Varona, Strategic Cloud Engineer at Google

Google Datacenters: GCP latencies of less than 40ms are not needed for Big Data

Speed: 8 TB of info can be moved from EU to USA in around 3 minutes

Useful Google Cloud components for Data Scientists:

* Compute
  * App Engine: front end for projects
  * GPU

* Google Cloud Storage:
  * Data Scientists should use Standard/Regional for Big Data
  
* Serverless Computing
  * Cloud Functions - App Engine - Cloud Run
  
* Developer Tools
  * Code repositories
  
* Data Analytics - Big Data
  * Big Query (Data Warehouse: Distributed Storage + Search Engine) (e.g. evaluates 7 TB data queries in 7 seconds)
  
* AI and Machine Learning

Use Google Chrome when possible

When using Google Cloud Storage, install the client in the local server and upload the files in multi-threads

Use Google Cloud Pricing Calculator for having an idea about costs

### GCP and Big Data

GCP for DS focuses in the programming, not on the underlying infrastructure

### Pub/Sub

Real-time messaging with mid-speed latency. Usually used on JSON format. 40USD/month for 1 TB messages

Saves the messages for 7 days. Have to be saved in another storage for keeing them longer 

Push or pull

Only useful for specific needs of reat-time appliccations, otherwise it's too expensive

### Dataflow

Programming languages Java - Python - Scala

E(xtraction)T(trasfer)L(oading) - Analysis - Orchestration

Dataflow is recommended for Stream processing

### Dataproc

Advantages over Hadoop/Spark: not idle clusters, scaling flexibility

### BigQuery

Parallel prcessing, memory processing (like Spark), shared memory (thousand of shared nodes, like a datalake)

Worker: processing unit - half-processor and 1 GB RAM, will perform the tasks 

Costs: on demand or flat rate, per volume of processed data

Recommended - alwas 3 layers minimum in data lakes:

* Raw data
* Processed data (1 or more layers, depending of processes complexity)
* Reporting data

Infinite storage capacity

Google maintains the cluster and only charges per consult, 5 USD per 1 TB processed

Pricing:
* Storage 
	* 0,20 USD/1 TB/month. From 90 days, 0.20 USD /1 TB/month. First 10 TB free
	* Ingest rate of streming data

* Processing
	* 5 USD/1 TB (first 1 TB free)
	* Flat-rate plans recommended from 5,000 - 10,000 USD

There are BigQuery public datasets available (v.g. AccuWeather)

2,000 slots = 100-1000 daily users making queries, 50 concurrent queries

Recommended partitioning tables over per day/month/year

For relational tables, it is recommended to do the queries in joined tables (after nightly join batches)

BigQuery is oftend use with Google CLI (command line)
https://cloud.google.com/bigquery/docs/bq-command-line-tool

Or used in automatic processes with Composer

### Dataprep

Useful for quickly pre-processing data before the queries

### Colab

* Benefits: free, integrated with BigQuery and CloudML. Useful for VMs with pre-installed libraries
* Cons: sometimes there is not powerful enoguh, not to be used in production environments
