---
title: "Introduction & Loading the Data"
teaching: 30
exercises: 5
---

:::::::::::::::::::::::::::::::::::::: questions

- What does "machine learning" mean, and how is it different from the hypothesis
  tests you already know?
- What are features (`X`) and a target (`y`) in a clinical dataset?
- How do we load the dataset and the Python libraries we'll use for the rest of
  the workshop?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Define machine learning as finding patterns in historical data to make
  predictions about new data.
- Distinguish features (`X`) from a target variable (`y`) in tabular data.
- Import the Python libraries used throughout this workshop.
- Load the breast cancer dataset into a pandas DataFrame.

::::::::::::::::::::::::::::::::::::::::::::::::



## What is machine learning?

You already know how to ask "does group A differ from group B?" with a t-test or
an ANOVA. Machine learning (ML) asks a different question: **given everything we
know about a patient, can we predict an outcome we don't yet know?**

A simple, non-technical definition: ML is *finding patterns in historical data to
make future decisions*.

A useful analogy: a machine learning model is like a medical resident who has
reviewed hundreds of past patient files. When a new patient walks in, the
resident recognises the pattern from cases they've seen before. The model isn't
"reasoning" the way a clinician does. It's pattern-matching at scale.

Two pieces of vocabulary we'll use for the rest of the workshop:

- **Features (`X`)** -- the measurements/predictors for each patient (what you'd
  already call covariates).
- **Target (`y`)** -- the outcome we want to predict (here: malignant or benign).

:::::::::::::::::::::::::::::::::::::: instructor

Ask the room how they'd normally test whether two patient groups differ, then contrast 
that with "predict the outcome for one new, individual patient."

::::::::::::::::::::::::::::::::::::::::::::::::::

## Importing the libraries

We'll use five Python libraries throughout this workshop:

- [`pandas`](https://pandas.pydata.org/) -- loading and working with tabular data
- [`numpy`](https://numpy.org/) -- numerical operations
- [`matplotlib`](https://matplotlib.org/) and [`seaborn`](https://seaborn.pydata.org/) -- plotting
- [`scikit-learn`](https://scikit-learn.org/) -- the dataset, preprocessing, PCA, and the model itself

In Google Colab these are already installed, so importing them is all you need
to do:


``` python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

sns.set_style("whitegrid")   # a clean default look for all our plots

print("pandas version:", pd.__version__)
```

``` output
pandas version: 3.0.6
```

## Loading the data

We're using the **Breast Cancer Wisconsin (Diagnostic)** dataset, which ships
directly with scikit-learn. It has 569 patients with features derived from digitised
images of fine needle aspirate (FNA) biopsies (e.g. cell nucleus radius, texture,
smoothness). The target is binary: malignant vs. benign.

::::::::::::::::::::::::::::::::::::: callout

This is a clean, engineered teaching dataset, not messy real-world clinical
data. Real data usually has missing values, class imbalance, and inconsistent
coding. It's worth keeping this in mind so this doesn't look like "how easy real
clinical ML is."

::::::::::::::::::::::::::::::::::::::::::::::::


``` python
from sklearn.datasets import load_breast_cancer

data = load_breast_cancer()
df = pd.DataFrame(data.data, columns=data.feature_names)
df['diagnosis'] = data.target                                    # 0 = malignant, 1 = benign
df['diagnosis_label'] = df['diagnosis'].map({0: 'Malignant', 1: 'Benign'})

df.head()
```

``` output
   mean radius  mean texture  ...  diagnosis  diagnosis_label
0        17.99         10.38  ...          0        Malignant
1        20.57         17.77  ...          0        Malignant
2        19.69         21.25  ...          0        Malignant
3        11.42         20.38  ...          0        Malignant
4        20.29         14.34  ...          0        Malignant

[5 rows x 32 columns]
```

Rows are patients, columns are features plus our target (`diagnosis`).

We've also added a `diagnosis_label` column. The model only ever needs the
numeric `diagnosis` column, but readable labels make plots and summary tables
much easier to discuss, and we'll rely on them from the next episode onwards.

::::::::::::::::::::::::::::::::::::: challenge

## Challenge 1: Features and target

In the DataFrame you've just created, which columns are the features (`X`) and
which is the target (`y`)?

And in your own research, what would the equivalent of each be?

:::::::::::::::::::::::: solution

The 30 measurement columns (`mean radius`, `mean texture`, and so on) are the
**features** or the inputs the model will learn from. The `diagnosis` column is
the **target** or the outcome we're trying to predict.

In your own work, the features are whatever you measured for each sample or
patient, and the target is the outcome you'd like to predict for a new one.
If you're used to regression modelling, features are your predictors or
covariates, and the target is your response variable.

:::::::::::::::::::::::::::::::::
::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::: instructor

Check-in point: Confirm everyone can see the DataFrame rendered as a table
before moving on to exploratory data analysis in the next episode.

::::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: keypoints

- Machine learning finds patterns in historical data to predict outcomes for
  new cases, rather than testing whether groups differ on average.
- Features (`X`) are the predictors; the target (`y`) is the outcome we're
  trying to predict.
- `pandas`, `numpy`, `matplotlib`, `seaborn`, and `scikit-learn` are all we
  need, and all come pre-installed in Google Colab.
- The breast cancer dataset loads directly from `sklearn.datasets` -- no file
  download required.

::::::::::::::::::::::::::::::::::::::::::::::::
