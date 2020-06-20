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

* price of flight - or better ratio price vs. average historic price of that route
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

Variables can be TRANSACTIONAL (related to features of the process) or USER RELATED (describe the user's habits)

On e-commerce websites, HITs with positive outcome are very reduced. Oversampling or undersampling could be used, but should be avoided as are artificial methods. **So changing the time intervals of the observed data and adding those observations as new users can be very useful.**

Observation 1: behavior days -60 and -30, analyzed purchases between days -30 and -15

Observation 2: beahavior days -67 and -37, analyze purchases between days -37 and -22

#### Evaluating the model

**High accuracy** does not mean the model is good, as data can be imbalaced

**High precision** does not mean that the model is financially viable. Precision ideally would be useful for fraud detection, but can have bias as labeling is human based. Precision for delinquency detection

**High recall added to high precision** means the model is financially viable. Recall useful for fraud detection without bias

Sensitivity = Recall

False positive rate = 1 - Especificity

### Cost matrix

It is similar to the confusion matrix except the fact that we are calculating the cost of wrong prediction or right prediction. Useful for assesing risk of marketing campaigns, e.g.

