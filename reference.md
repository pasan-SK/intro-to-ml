---
title: 'Reference'
---

## Glossary

**Feature (`X`)**
: An independent variable or predictor used as input to a model — what you'd
normally call a measurement or covariate (e.g. tumour radius, texture).

**Target (`y`)**
: The outcome a model is trained to predict (e.g. malignant vs. benign).

**Supervised learning**
: Training a model on historical cases where the outcome (`y`) is already
known, so it can predict that outcome for new, unseen cases.

**Train/test split**
: Holding back a portion of the data (the test set) that the model never sees
during training, so it can be evaluated honestly afterwards.

**Overfitting**
: When a model learns the training data too specifically, including its
noise, and performs well on it but poorly on new, unseen data.

**Data leakage**
: When information from the test set influences training (e.g. fitting a
scaler on the full dataset instead of training data only), making evaluation
results optimistically biased.

**Feature scaling / `StandardScaler`**
: Rescaling every feature to the same footing (mean 0, comparable spread), so
features measured in different units don't dominate a model purely because of
their numeric scale.

**Principal Component Analysis (PCA)**
: A technique that compresses many correlated features into a smaller number
of components that preserve as much of the original variation as possible,
useful for visualising high-dimensional data.

**Explained variance**
: The proportion of the original data's total variation captured by a given
principal component.

**Decision tree**
: A model that makes a prediction through a series of yes/no splits on
feature values (e.g. "is radius > 15?").

**Random Forest**
: An ensemble of many decision trees, each trained on a random subset of the
data and features, whose predictions are combined by majority vote.

**Confusion matrix**
: A table counting the four possible outcomes of a classifier's predictions
against the true labels: true positives, true negatives, false positives, and
false negatives.

**Sensitivity**
: Of all patients who actually have the condition, the proportion the model
correctly identified.

**Specificity**
: Of all patients who do not have the condition, the proportion the model
correctly cleared.

**Feature importance**
: A score, derived from a trained model (e.g. a Random Forest), indicating how
much each feature contributed to its predictions. Reflects statistical
reliance, not biological causation.
