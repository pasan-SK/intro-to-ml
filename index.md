---
site: sandpaper::sandpaper_site
---

Machine learning is increasingly part of clinical and life science research, but
most introductions to it are written for computer scientists. This workshop is
written for the rest of us.

Over three hours you will take a real clinical dataset: 569 breast tissue
biopsies and build a working, interpretable classifier that predicts whether a
tumour is malignant or benign. Along the way you'll see why the familiar
hypothesis tests you already use answer a fundamentally different question from
the one machine learning asks, and you'll come away able to tell which tool a
given research question actually needs.

No mathematics beyond what you already use in your own analyses. No local
software installation because everything runs in Google Colab in your browser.

## What you'll learn

By the end of this workshop you will be able to:

- Identify features (`X`) and target variables (`y`) in clinical tabular data.
- Preprocess and scale data using `pandas` and `scikit-learn`.
- Apply Principal Component Analysis (PCA) to visualise high-dimensional data.
- Train and evaluate a Random Forest classifier.
- Interpret feature importance to guide real measurement decisions.
- Explain why accuracy alone is an inadequate measure of a clinical model.

## Who this is for

Life scientists, clinicians, and clinical researchers who are comfortable with
data analysis but new to predictive modelling. If you have ever run a t-test or
an ANOVA and wondered what "machine learning" would add, this workshop is aimed
squarely at you.

:::::::::::::::::::::::::::::::::::::::::: prereq

## Prerequisites

You'll get the most out of this workshop if you already have:

- **Basic Python syntax** - variables, lists, and dictionaries.
- **Basic pandas** - loading a CSV and viewing a DataFrame.

You do **not** need any prior experience with machine learning, statistics
beyond introductory level, or any local software setup. Please see the
[Setup](learners/setup.md) page before the workshop begins.

::::::::::::::::::::::::::::::::::::::::::::::::::

## About this lesson

This lesson is built with the
[Melbourne Bioinformatics fork](https://github.com/melbournebioinformatics/workbench-template-rmd)
of the [Carpentries Workbench](https://carpentries.github.io/sandpaper-docs).

For more information on Melbourne Bioinformatics, please see our
[official page](https://mdhs.unimelb.edu.au/melbournebioinformatics) and our
[tutorial collection](https://melbournebioinformatics.github.io/MelBioInf_docs/).
If you would like to attend one of our workshops, follow our
[Eventbrite page](https://www.eventbrite.com.au/d/australia--melbourne/melbourne-bioinformatics/),
where you can get notifications and register for upcoming workshops.
