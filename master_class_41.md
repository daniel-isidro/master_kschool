# Big Data - Spark 
## Toni Almagro, DS, Amadeus

**TIP** Use ```df.count()``` to check an action has been applied to all rows of a spark DataFrame. Do not use ```df.show()```

### ML Pipelines in Spark

ML model training and tuning often represents running the same steps once and again. Often, we run the same steps with small variations in order to evaluate combinations of parameters.

In order to make this use case a lot easier, Spark provides the Pipeline abstraction.

A Pipeline represents a series of steps in the processing of a dataset. Each step is a Transformer or an Estimator. The whole Pipeline is an Estimator, so we can .fit the whole pipeline in one step. When we do that, the steps' .fit and .transform methods will be called in turn.

**TIP** When doind string indexer, rename columns with ```_index```, and the same for one-hot encoded columns, they should end with ```_onehot```

**TIP** For showing what parameters have been selected ```split_model_chosen.bestModel.stages[-1].extractParamMap()```

**TIP** Use UDF for segmenting numeric values into segment values

**TIP** Use ```%store``` to share vars between Jupyter notebooks. Rename the vars to not overwrite them in the second notebook

Publish vars:
```python
fpr_new = fpr
tpr_new = tpr
%store fpr_new, tpr_new
```

To retrieve vars:
```python
%store -r
```

### Spark jobs in Google Cloud Platform

* You can work with the web console or with the terminal (installing gcloud SDK)
```gcloud init```

* Create cluster: Console -> Storage -> Create Bucket

* Use dataproc type clusters in GCP to use spark on them

```gcloud dataproc clusters create $CLUSTERNAME --region $REGION```

* View cluster: Console -> Big Data -> Clusters
