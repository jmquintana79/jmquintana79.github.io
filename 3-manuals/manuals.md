---
title: Manuales
has_children: true
nav_order: 3
---

# Manuales

Aquí serán incluidos manuales, anotaciones y demás que vaya escribiendo. Todo lo que sean articulos ó documentanciones que considere interesanes las iré listando aquí por temas.

## DATA HANDLING


### Data format

- [Feather File Format](https://www.journaldev.com/53105/feather-file-format-in-python)

```
# save data as feather file format
df.to_feather('filename.feather')
 
# read feather file
df1 = pd.read_feather('filename.feather')
```

### Missing values imputation

- [*sklearn* - Imputation of missing values.](https://scikit-learn.org/stable/modules/impute.html)
    - Univariate feature imputation.
    - Multivariate feature imputation.
    - Nearest neighbors imputation.
    - Marking imputed values.
    
### Data discretization: continuous to discrete values

- [*sklearn* - *sklearn.preprocessing.KBinsDiscretizer*](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.KBinsDiscretizer.html): Bin continuous data into intervals. It is available three possible strategies: ‘uniform’, ‘quantile’, ‘kmeans’.


## Machine Learning PIPELINES

- [*TowardsDataScience* - Creating Custom Transformers with Scikit-Learn](https://towardsdatascience.com/creating-custom-transformers-using-scikit-learn-5f9db7d7fdb5)