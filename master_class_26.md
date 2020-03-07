# Intro to Recommendation Engines

## Juan Arévalo, Cepsa

### Off Topic on Deep Learning

* Recommended reading: Judea Pearl, "The book of why". He is credited for developing a theory of causal and counterfactual inference based on structural models. He introduces "what-if" questions, what would had happened if we had introduced a different input variable. He does it with "Do-calculus".

### Interpretability vs Explainability

* Interpretability means knowing the mathematical equations under the models. 

* Explainability means knowing that certain inputs will lead to certain outputs, and what the most influential input variables are. Human Machine Interfaces study explainability.

### Metrics

* ```recall@n``` does not consider the order of the items. ```map@n``` does

* recall@n should never reach 1. Very good values (interesction between true positives and items rated in the test set) are around 0.3 (30%).

* Usually on the recommended output you'd have to remove the items that are on the training set. For example, so the recommended movies are not movies already seen. Exceptions are retailers, loyalty campaigns, etc., where you would like to see again the most bought products, most loyal customers again.

### Collaborative Filtering

* *Co-ocurrence matrices* are always squared (items vs items, users vs user, etc.). The popularity algorithm is in the trace of the matrix

