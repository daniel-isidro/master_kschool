# Supervised Learning - Regression
## Toni Almagro, Data Scientist, Amadeus

* Unsupervised Learning - Clustering example: k-means

* Unsupervised Learning - Dimensionality Reduction: intermediate step for other ML tasks

* Supervised Learning - Regression: Continuous variable **(NUMBER)**

* Supervised Learning - Classification: Categorical variable **(LABEL)**

* 90% of time used in ML problems is used on cleaning the features

* ML: FEATURES + MODEL + METRICS

* **All ML problems are about minimization, maximization, or optimization**

* **There are no best models, there are better models than others depending on the metrics**

* Labelled Training Data: Input vectors are usually matrices (several features)

* Objective is the relation between input and output vectors

* Classification: always start by logistic regression

* Metrics are different between regression and classification

* In k nearest neighbors, for multiple variables inputs, always normalize the input features to avoid different scales between them

* Having a **low MAE but a high RMSE** means we have several points that the model cannot predict well (outliers or not outliers). It makes sense using both metrics together

* We'll use cross validation so the train/test split has a minimum impact on the model

* The RMSE with cross validation is not necessary lower that without CV. But the model is more robust with CV

