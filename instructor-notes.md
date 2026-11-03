---
title: 'Instructor Notes'
---

This page collects general guidance for running the workshop as a whole.
Timing and talking points specific to a single episode live as instructor
notes inline within that episode, and are also aggregated automatically on
this site's Instructor Notes listing.

## Format

Three hours total, delivered as five episodes in Google Colab. No local
installation; see the [Setup](../learners/setup.md) page.

| Time | Episode | Focus |
|---|---|---|
| 0:00–0:30 | 01 Introduction & Loading the Data | The no-math framing, library imports, loading the dataset |
| 0:30–1:00 | 02 Exploratory Data Analysis | Pairplot, "can you draw a line?", train/test split |
| 1:00–1:45 | 03 Scaling & PCA | The scale problem, `StandardScaler`, dimensionality reduction |
| 1:45–2:25 | 04 Predictive Modeling | Random Forest, training, confusion matrix, sensitivity/specificity |
| 2:25–2:40 | 05 Feature Importance | `feature_importances_`, wrap-up |

## Audience

Life scientists, clinicians, and clinical researchers who are comfortable
with data analysis (they already run t-tests or ANOVAs) but new to predictive
modelling. See [Learner Profiles](../profiles/learner-profiles.md) for more
detail. Assume basic Python and pandas, nothing more.

## Running themes to reinforce throughout

- **Different question, not a better one.** A t-test asks whether two groups
  differ on average; a classifier predicts the outcome for one new patient.
  Come back to this contrast whenever the room seems to be evaluating ML
  against the standard of a hypothesis test.
- **The resident analogy.** A model is like a resident who has reviewed
  hundreds of past patient files and recognises patterns from them — not
  "reasoning," but pattern-matching at scale. Reused again in episode 4 (one
  tree = one resident's opinion, a forest = a room full of residents voting).
- **Visual evidence before formal modelling.** The pairplot in episode 2
  shows no single feature separates the classes; the PCA plot in episode 3
  shows that combining all of them does. The classifier's job is then just to
  formalise a boundary the room has already half-seen with their own eyes.

## Pacing tips

- Keep explanatory text light and let the discussion questions in each
  episode's `challenge` blocks do the work — they're designed to generate
  genuine debate (e.g. "which error is worse, a false positive or a false
  negative?"), not to be answered too quickly.
- The confusion-matrix and feature-importance discussions in episodes 4–5
  reliably run long with clinically-minded audiences. If you're short on
  time, these are the sections to compress rather than the hands-on coding.
- Leave real room for Q&A at the very end rather than rushing the recap —
  it's also your best source of signal on whether the pacing worked, for next
  time.
