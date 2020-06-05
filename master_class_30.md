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
