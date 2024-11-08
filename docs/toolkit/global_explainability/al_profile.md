---
layout: default
title: xrai_toolkit.global_exp.global_exp.al_profile
parent: Global Explainability
grand_parent: Toolkit
nav_order: 1
---

# xrai_toolkit.global_exp.global_exp.al_profile
**[xrai_toolkit.global_exp.global_exp.al_profile(exp, variables = None, var_type = 'numerical', groups = None, random_state = 42, N = 300, labels = False)](https://github.com/gaberamolete/XRAIToolkit/blob/main/global_exp/global_exp.py)**


Creates a accumulated-local plot and outputs the equivalent table. User may specify the variables to showcase. Note that this can only help explain variables that are of the same data type at the same time, i.e. you may not analyze a numerical and categorical variable in the same run.


**Parameters:**
- exp: explanation object
- variables: list, list of variables to be explained utilizing the methods. The default is 'None', which will make it run through all variables.
- var_type: can either be 'numerical' or 'categorical'.
- groups: specify a single categorical variable not in the 'variables' list that will be used as a group. Defaults to 'None'.
- random_state: defines the random state in which the number of observations to be sampled. Defaults to 42 for reproducibility.
- N: Number of observations to be sampled with. Defaults to 300. Writing 'None' will have the function use all data, which may be computationally expensive.
- labels: boolean. If True, will change label to 'PD profiles'.

**Returns:**
- result: DataFrame of the results from the accumulated-local profile plot.
- plot: plotly.Figure for the visualization