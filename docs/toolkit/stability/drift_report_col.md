---
layout: default
title: xrai_toolkit.stability.stability.data_drift_column_report
parent: Stability
grand_parent: Toolkit
nav_order: 1
---

# xrai_toolkit.stability.stability.data_drift_column_report
**[xrai_toolkit.stability.stability.data_drift_column_report(current_data, reference_data, column, report_format = 'json', stattest = None, stattest_threshold = None)](https://github.com/gaberamolete/xrai_toolkit/blob/main/stability/stability.py)**


This evaluates the data drift in one column of the current dataset.
    
Drift detection methods that can be used for `stattest` and other equivalent parameters are as follows:
- `ks`: Kolmogorov-Smirnov test, only numerical. Returns p_value drift detected when less than threshold (default is 0.05).
- `chisquare`: Chi-Square test, only categorical. Returns p_value drift detected when less than threshold (default is 0.05).
- `z`: Z-test, only categorical. Returns p_value drift detected when less than threshold (default is 0.05).
- `wasserstein`: Normalized Wasserstein distance, only numerical. Returns distance drift detected when greater than or equal to threshold (default is 0.1).
- `kl_div`: Kullback-Leibler, numerical and categorical. Returns divergence drift detected when greater than or equal to threshold (default is 0.1).
- `psi`: Population Stability Index, numerical and categorical. Returns psi_value drift detected when greater than or equal to threshold (default is 0.1).
- `jensenshannon`: Jensen-Shannon distance, numerical and categorical. Default method for categorical, if there are > 1000 objects. Returns distance drift detected when greater than or equal to threshold (default is 0.1).
- `anderson`: Anderson-Darling test, only numerical. Returns p_value drift detected when less than threshold (default is 0.05).
- `fisher_exact`: Fisher's Exact test, only categorical. Returns p_value drift detected when less than threshold (default is 0.05).
- `cramer_von_mises`: Cramer-Von-Mises test, only numerical. Returns p_value drift detected when less than threshold (default is 0.05).
- `g-test`: G-test, only categorical. Returns p_value drift detected when less than threshold (default is 0.05).
- `hellinger`: Normalized Hellinger distance, numerical and categorical. Returns distance drift detected when greater than or equal to threshold (default is 0.1).
- `mannw`: Mann-Whitney U-rank test, only numerical. Returns p_value drift detected when less than threshold (default is 0.05).
- `ed`: Energy distance, only numerical. Returns distance drift detected when greater than or equal to threshold (default is 0.1).
- `es`: Epps-Singleton tes, only numerical. Returns p_value drift detected when less than threshold (default is 0.05).
- `t_test`: T-Test, only numerical. Returns p_value drift detected when less than threshold (default is 0.05).
- `emperical_mmd`: Emperical-MMD, only numerical. Returns p_value drift detected when less than threshold (default is 0.05).
- `TVD`: Total-Variation-Distance, only categorical. Returns p_value drift detected when less than threshold (default is 0.05).
A combination of these tests are used if `stattest` and other equivalent parameters are not explicitly specified.


**Parameters:**
- current_data: DataFrame, inference data collected after model deployment or training.
- reference_data: DataFrame, dataset used to train your initial model on.
- column: Column from both current and reference data to detect drift on.
- report_format: Specify the format to output the report object in, from `json`, `dict`, and `DataFrame`. Defaults to `json`.
- stattest: Defines the drift detection method for a given column (if a single column is tested), or all columns in the dataset (if multiple columns are tested).
- stattest_threshold: Sets the drift threshold in a given column or all columns. The threshold meaning varies based on the drift detection method, e.g., it can be the value of a distance metric or a p-value of a statistical test.

**Returns:**
- data_drift_report: Interactive visualization object containing the data drift report
- ddr: Report 