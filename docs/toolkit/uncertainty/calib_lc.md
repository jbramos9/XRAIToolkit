---
layout: default
title: xrai_toolkit.uncertainty.calibration.calib_lc
parent: Uncertainty
grand_parent: Toolkit
has_children: false
nav_order: 1
---

# xrai_toolkit.uncertainty.calibration.calib_lc
**[xrai_toolkit.uncertainty.calibration.calib_lc(y_pred,y_true,reg)](https://github.com/gaberamolete/xrai_toolkit/blob/main/uncertainty/calibration.py)**


Logistic Calibration, also known as Platt scaling, trains an SVM and then trains the parameters of an additional sigmoid function to map the SVM outputs into probabilities.


**Parameters:**
- y_pred (numpy.ndarray): Array or series of predicted values.
- y_true (numpy.ndarray): Array or Series with ground truth labels.
- reg (bool): Determines if y's given are from a regression or classification problem. Defaults to False.

**Returns:**
- lc: Logistic Calibration object.
- lc_calibrated: Recalibrated values under Logistic Calibration, given via array.
