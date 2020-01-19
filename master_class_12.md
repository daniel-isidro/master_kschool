# Master Class 12 - Modeling Methodology

## Sébastien Pérez

Real value of data science/ML is adding value to existing solutions, more than state of the art innovative solutions.

Cloud solutions: 
* Saves the hassle of upgrading when the paradigm changes, always latest version
* Scalable
* Has ecosystem of services around it

99% of ML problems are solved with supervised learning (classification and regression, and clustering/segmentation) not unsupervised learning (reinforcement)

Reinforcement learning has a caveat: it needs human labelling

ML requires a table of features, one of the columns needs to be the label=target. It is meaning to find a relation between the features and the target, so it can make high probability predictions

* The real added value of a data scientist is in choosing the right features, finding the best parameter for the model. *

ML Models: linear regressions, decision trees

Choosing the right model means using on metric (mean of errors, etc.) and finding the model with the best metric

Summary: ML is about features, models and metrics

### Applying ML to business problems
1. First we have to select the business value and measure of success, which can be numbers = regression (v.g no. of customers), or labels = classification (v.g. yes/no)
2. Data sources
3. ML task + metric
4. Features extraction and model creation
5. Industrialization
    - When to use the model, when to train the model and when to reevaluate the model

### ML canvas
Value proposition
ML initiative cost : time to have the model running

### What to do when our best ML model is not satisfactory
1. Get more data
2. Add features
3. Remove features
    - Example: if we interchange the data of two columns(=features) and the result does not change much, those features may not be needed 
4. Try new models

### Improving the model
Once we’ve had a satisfactory prediction, we can choose one feature and slightly vary it to see if the predictions improve

### Business have two needs
1. How to get the data
2. How to use ML to solve solutions
