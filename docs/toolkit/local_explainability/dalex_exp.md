---
layout: default
title: xrai_toolkit.local_exp.local_exp.dalex_exp
parent: Local Explainability
grand_parent: Toolkit
nav_order: 1
---

# xrai_toolkit.local_exp.local_exp.dalex_exp
**[xrai_toolkit.local_exp.local_exp.dalex_exp(model, X_train, y_train, X_test, idx)](https://github.com/gaberamolete/xrai_toolkit/blob/main/local_exp/local_exp.py)**


Dalex-related explanation object.


**Parameters:**
- model: model object, full model, can be with preprocessing steps
- X_train: DataFrame
- y_train: DataFrame
- X_test: DataFrame
- idx: int, index

**Returns:**
- exp: explanation object
- obs: single Dalex-enabled observation