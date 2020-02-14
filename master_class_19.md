# Supervised Learning - Multiple Lineal Regression

## Marcio Encinar, PhD, Mapfre

### Multiple linear regression equation

* When solving the multiple linear regression equation, in the X matrix, we always have to use a column of 1s to get the \beta_0 regression coefficient (Y-axis crossing point)

* In multiple linear regression, collinearity is also something to avoid

* In MLR, the validity of the adjusted model is used through the adjusted R-squared (in simple LR it was R-squared)

* When using training and testing datasets, **the testing dataset cannot be used in the validation part of the training.** Else it would influence the model as it would do overfitting. Always have a test dataset to check, after selecting all the parameters, that the model works

### Outliers 

* It's good practice to code outliers as dummy (categorical) values, so you don't lose their information. Plus they don't skew the metrics (like median or mean), when converted to categorical

