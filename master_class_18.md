# Supervised learning - Linear regression
## Mario Encinar, PhD - Mapfre

* Inference (in Statistics) = Predictive ability (ML)

* Statistics is based on Mathematics, ML is based on algorithms

* ML is searching for the optimized relation between variables

* **Applied Data Science** means using the algorithms withouth fully understanding them

* Machine learning engineering goes deeper in the algorithms

### Machine learning - Supervised Learning
x,y

### Machine learning - Supervised Learning - Regression
y continuous

### Machine learning - Supervised Learning - Classification
y discrete

### R vs python

SAS is very efficient in data processing, but not good on ML

* **R is better in linear regression models** (lm, glm), though it also covers ML (decission trees, random forests, gradient boosting)

* **python is better in ML** (decission trees, random forests, gradient boosting, support-vector machine)

### Data Science phases

1. Data extraction + preprocessing (SQL, Hive, Joints...) (maybe done by Data Engineers)

2. Descriptive analysis, exploratory analysis, diagnostic analysis

3. Predictive analysis, prescriptive analysis

4. Production model (maybe done by Data Engineers)

### Linear regression

* **Regression problems** consist on exploring datasets, introducing a new variable, and predicting the outcome

* **Exploratory analysis** consist in looking at scatterplots or histograms and predicting the correlation between vars

* Errors have mean=0, var=constant, normal distribution, and are not dependant on the input variabless

* In linear regression models, **collinearity** between two input variables is affecting negatively to the results. But collinearity between input vars and the output is desired.

```cor(advertising) ```

* Collinearity over 0.7 between input vars and the output var can be considered as good enough. But for ML models low collinearities can also be used

* R-squared values close to 1 usually imply collinearity between the input var and the output var. Probably that input var depends on the output var. **Overlooking this is a common error for Data Scientists**

### Overfitting

* Making the regression too adjusted to the existing data can lead to overfitting. This should be avoided as this would not predict correctly new data points added to the existing dataset. Validation methods are used to avoid overfitting: dividing the dataset into training part and test part. We find the regression in the training part and later we apply it to the test past. To check the validity, we compare the MSE (mean square errors) in the train part versus the MSE in the test part.

### Statistical packages in python

* The equivalent for python to the R statistics functions is statsmodels

* For ML in python, the used packages are `scikit-learn` and `sklearn`

### Error metrics

* In linear regressions the error metric is MSE. In Classification the error metric is the confusion matrix (true positives and flase negatives)

