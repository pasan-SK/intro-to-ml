---
title: Setup
---

This workshop uses **Google Colab**, a free, browser-based notebook environment. There is
**nothing to install** on your own machine before the workshop.

## What you need

- A laptop with a modern web browser (Chrome, Firefox, Edge, or Safari).
- A Google account, used to open and run the Colab notebook. If you don't have one, you can
  create one for free at <https://accounts.google.com/signup>.
- Basic familiarity with Python syntax (variables, lists, dictionaries) and basic pandas
  operations (loading a CSV, viewing a DataFrame). 

## Software

All the Python packages used in this workshop: `pandas`, `numpy`, `matplotlib`, `seaborn`,
and `scikit-learn`. They come pre-installed in Google Colab, so no package installation is
required either.

::::::::::::::::: discussion

### Checking your Colab session works

Before the workshop, open a new notebook at <https://colab.research.google.com/> and run the
following in the first cell:

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import sklearn

print("pandas:", pd.__version__)
print("scikit-learn:", sklearn.__version__)
```

If this runs without error and prints version numbers, you're ready for the workshop.

::::::::::::::::::::::::::::

## Workshop notebook

<!-- FIXME: add the "Open in Colab" link to the Master Notebook here once it's published,
     e.g. a GitHub-hosted .ipynb with an Open in Colab badge, or a shared Google Drive link. -->

[Open the workshop notebook in Google Colab](FIXME)

## Data

This workshop uses the [Breast Cancer Wisconsin (Diagnostic) dataset](https://scikit-learn.org/stable/datasets/toy_dataset.html#breast-cancer-wisconsin-diagnostic-dataset),
which ships directly with scikit-learn. **There is no separate file to download** — it loads
straight into the notebook with:

```python
from sklearn.datasets import load_breast_cancer

data = load_breast_cancer()
```

We'll turn this into a pandas DataFrame together at the start of the workshop.

### Data citation

This dataset is distributed under a [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
license and should be credited as:

> Wolberg, W., Mangasarian, O., Street, N., & Street, W. (1993). Breast Cancer Wisconsin 
> (Diagnostic) [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5DW2B.

<!-- ## Cheat sheet -->

<!-- FIXME: link the one-page scikit-learn workflow cheat sheet (StandardScaler -> fit ->
     predict) here once it's prepared. -->
