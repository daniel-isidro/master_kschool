# Supervised Learning
### Toni Almagro, Data Scientist, Amadeus

## Supervised Learning - Regression

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

* Decsission trees are used to minimize the spread of the data

* For rating models we can use custom metrics (custom scorer). Custom mestric need input vector, prediction vector, and as a result they return a number

* To avoid overfiiting, you can use the train/test/validation splits. Otherwise validation set is not used

* **High bias** means the model is too simple for the data (underfitting), the model does not express the complexity of the data (for example, data that more or less behave like a parable expressed as a line). This may be solved increasing the complexity of the model

* **High variance** may mean the model has overfitting, that the model adjusts too well to the existing data, also to the noise of the existing data, so it will not be able to adusjt with precision to new data. This may be solved reducing the complexity of the model

## Supervised Learning - Classification

* Support Vector Machines are not generally used. It is used as a last resort method. It's trainig takes hours vs minutes in decission trees

* SVM is meant for finding a line that separates two classes. Margin is the error

## Gradient Boosting Trees

* It is a type of ensemble learning

* Can be used for regression and for classification

* Always use learning_rate=0.1
