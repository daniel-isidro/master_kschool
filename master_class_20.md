# Supervised Learning - Generalized Linear Models
## Mario Encinar, PhD, Mapfre

### Recap: Validating models

* In Linear Regression, Generalized Linear Models, Advanced Regression: with error factors

* With Machine Learning: with cross-validation

### Recap: LR Objective

* Minimizing the loss function. We can get exact coefficients for the loss function

* Optimization of the objective function: basic algorithm - gradient descent

### Maximum Likelihood Estimation

* In a lineal regression, all the x-dependent y values are behaving like a random value fitting in a normal distribution. MLE is used for adjusting models

### GLMs

* Can be applied to regression problems and also to classification problems

* In GLMs you have to choose a distribution to explain the model

* Three factors: random component (to what distribution it belongs), systematic component, link function. We only have to choose systm and link, the other is a given

* In the Titanic dataset, the mean of survivors is 0.38. The naif model where nobody survived, it is only 62% accurate. That is why **accuracy is never a good metric**

* For getting a model in R, we must convert the categorical values to factors:
`titanic$Sex <- as.factor(titanic$Sex)`

* In the Titanic exercise, Pclass1 is not included in the model as it is a combination of Pclass2 and Pclass2. Same with Sexfemale, it is complentary to Sexfemale

* Intercept is \beta_0, the crossfing point with Y-axis

* **Factors do not exist in python**, you have to convert categorical values into binary values

### ROC curve

* Validation technique for classification model 
* Sensitivity = true positive rate (TPR)
* Specificity = true negative rate (TNR)
* ROC curves can be adjusted with different thresholds, depending on the desired proximity to true positives or true negatives
* The area under the curve is independent from the threshold
* Mario always uses ROC with Sensitivity vs 1-Specificity

# Validation

* The package `caret` is the equivalent in R to `sklearn` in python. It is olnly maintained by one person, so watch out for bugs or weird outputs
* `caret` is a wrapper package that integrates other packages (like `glm`)
* `caret` uses 0.5 by default as threshold. Cannot be modified (it can in `sklearn`)
* Mario recommends using `sklearn` in python for glm, as the methods of validation are clearer than those of `caret`
