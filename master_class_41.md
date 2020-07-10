# Big Data - Spark 
## Toni Almagro, DS, Amadeus

**TIP** Use ```df.count()``` to check an action has been applied to all rows of a spark DataFrame. Do not use ```df.show()```

**ML Pipelines in Spark**

ML model training and tuning often represents running the same steps once and again. Often, we run the same steps with small variations in order to evaluate combinations of parameters.

In order to make this use case a lot easier, Spark provides the Pipeline abstraction.

A Pipeline represents a series of steps in the processing of a dataset. Each step is a Transformer or an Estimator. The whole Pipeline is an Estimator, so we can .fit the whole pipeline in one step. When we do that, the steps' .fit and .transform methods will be called in turn.
