# Supervised Learning - Generalized Linear Models
## Mario Encinar, PhD, Mapfre

### Recap: Validating models

* In Linear Regression, Generalized Linear Models, Advanced Regression: with error factors
* With Machine Learning: with cross-validation

### Recap: LR Objective

* Minimizing the loss function. We can get exact coefficients for the loss function
* Optimization of the objective function: basic algorithm - gradient descent

### GLMs

* Can be applied to regression problems and also to classification problems
* In GLMs you have to choose a distribution to explain the model
* Three factors: random component (to what distribution it belongs), systematic component, link function. We only have to choose systm and link, the other is a given

### Maximum Likelihood Estimation

* In a lineal regression, all the x-dependent y values are behaving like a random value fitting in a normal distribution. MLE is used for adjusting models

** In titanic dataset, the mean of survivors is 0.38. The naif model, nobody survived, is only 62% probably correct. That is why **accuracy is never a good metric**



