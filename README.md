# DSCI 552 — Homework 4

Jesse Ngo

Time series classification on the UCI AReM (Activity Recognition based on Multisensor data fusion) data, Part 2: binary classification of bending vs. other activities with logistic regression (RFE feature selection, case-control sampling) and L1-penalized logistic regression, then multiclass classification with L1-penalized multinomial regression and Naive Bayes (Gaussian and multinomial). Also ISLR exercises 4.8.3 and 4.8.7. The Part 1 feature extraction code from Homework 3 is included in the notebook because Part 2 builds on it.

## Structure

```
.
├── README.md
├── .gitignore
├── requirements.txt
├── data
│   └── AReM
│       ├── bending1 ... walking   (one folder per activity, datasetN.csv per instance)
│       ├── bendingType.pdf
│       └── sensorsPlacement.pdf
└── notebook
    └── Ngo_Jesse_HW4.ipynb
```

## Running

```
pip install -r requirements.txt
```

Open `notebook/Ngo_Jesse_HW4.ipynb` in Jupyter and run all cells (about 5 minutes; the cross-validation over l = 1..20 is the slow part). The data is loaded with the relative path `../data/AReM`. Three data files were cleaned by hand: `bending2/dataset4.csv` (spaces replaced with commas) and `cycling/dataset9.csv`, `cycling/dataset14.csv` (trailing comma removed).

## Data

AReM dataset, UCI Machine Learning Repository:
https://archive.ics.uci.edu/ml/datasets/Activity+Recognition+system+based+on+Multisensor+data+fusion+%28AReM%29
