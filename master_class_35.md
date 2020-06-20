# Business Analytics, Geo Analytics and Machine Learning with BigQuery
## Alex Urcola, Google
### BigQuery
**Tip:** select specific columns when doing queries, for cheaper queries

### Standard SQL Basic Concepts
**Tip:** Search for "bigquery public datasets" in Google search
* In BigQuery Editor, click on 'More - Format' for prettifying the code

* '--' for commenting code lines or '/* abcdef */' for commenting code chunks

* Run various scripts in parallel:
```
BEGIN
query1
query2
END
```

### ML for Analysts

Practical Case - Iberia and Google's BigQuery

https://www.thinkwithgoogle.com/intl/es-es/canales-de-publicidad/tecnologia-emergente/iberia-utiliza-el-poder-del-machine-learning-para-identificar-clientes-de-gran-valor/

**Target:** Predict whether a user would purchase a flight in the next 15 days, after analyzing their data of the past 30 days. New marketing campaigns would be targeted to specific users and to probable soon-to-be flight buyers.

**Data** can be clicks, scrolling, time spent at pages, etc. Every user session can generate 1000 lines of data.

**Data table**

Every user interaction (click, scroll...) is considered a HIT

Every HIT (row) has nested fields

Every SESSION has several HITs

Since data is sparse (a lot of zeros, just a few few flights of the thousands shown are bought), we have to generalize/simplify the data

We can focus on several fields to simplify the data:

* popular routes
* popular destinations
* classficate by short/medium/long routes 
* trip length (business/leisure)
* number of passengers
* frequent flier
* has purchased in the past or not
* latest purchase process step achieved
* number of visits last 30 days - visits days 30-21 - visits days 20-11 - visits days 0-10
* weekday of flight
* time of flight

This model will be based on COOKIES, not on users (a user in a different device generates a new cookie)

Variables can be TRANSACTIONAL (related to the process features) or USER RELATED (describe the user's habits)
