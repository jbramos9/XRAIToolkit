---
layout: default
title: xrai_toolkit.global_exp.global_exp.dalex_exp
parent: Global Explainability
grand_parent: Toolkit
nav_order: 1
---

# xrai_toolkit.global_exp.global_exp.dalex_exp
**[xrai_toolkit.global_exp.global_exp.dalex_exp(model, X_train, y_train, X_test, idx)](https://github.com/gaberamolete/xrai_toolkit/blob/main/global_exp/global_exp.py)**


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