---
layout: default
title: xrai_toolkit.local_exp.local_exp.get_feature_names
parent: Local Explainability
grand_parent: Toolkit
nav_order: 1
---

# xrai_toolkit.local_exp.local_exp.get_feature_names
**[xrai_toolkit.local_exp.local_exp.get_feature_names(column_transformer, cat_cols)](https://github.com/gaberamolete/xrai_toolkit/blob/main/local_exp/local_exp.py)**


Get feature names from all transformers.


**Parameters:**
- column_transformer (sklearn.ColumnTransformer): Extract the column transformer from the model
- cat_cols (List(str)): Column names for categorical variable

**Returns:**
- feature_names (List(str)): Names of the features produced by transform.
