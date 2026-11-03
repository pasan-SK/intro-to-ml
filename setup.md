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

## Running the materials on your own device

You also can install of the packages on your own device if you prefer. Make sure that Python is already installed by using the command:

```bash

python --version

```
You should be able to see which Python version you have installed. If Python is not installed, you will get an error.

You can use `pip` or `conda` to install the Python packages used in this workshop using the terminal. You can use the following code if you have `pip` installed:

```bash

pip install pandas numpy matplotlib seaborn scikit-learn

```

You can read more about installing Python packages [here](https://packaging.python.org/en/latest/tutorials/installing-packages/). You can also read the instructions on installing `scikit-learn` specific to your device and preferred installing on their website [here](https://scikit-learn.org/stable/install.html).

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

[Open the workshop notebook in Google Colab](https://colab.research.google.com/drive/15TfwZDd9MNx4P8ui1_zQa8vws7eUC70v)

When you open it, go to **File → Save a copy in Drive** before editing, so your
changes don't affect the shared master copy.

## Data

This workshop uses the [Breast Cancer Wisconsin (Diagnostic) dataset](https://scikit-learn.org/stable/datasets/toy_dataset.html#breast-cancer-wisconsin-diagnostic-dataset),
which ships directly with scikit-learn. **There is no separate file to download**. It loads
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
