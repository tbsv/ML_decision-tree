# Machine Learning // Decision Tree

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/tbsv/ML_decision-tree/master?filepath=decision-tree_solution.ipynb)

This is Binder-compatible repo with a `requirements.txt` file.

## Summary

//TODO summary

## Contents

There is 1 notebook in this repository:

- [decision-tree_solution.ipynb](decision-tree_solution.ipynb) : runs a decision tree exercise that is taken from a Udemy course (see details in the *About* section below).

In addition, the following ressources are in this repository:

- [requirements.txt](requirements.txt) : lists all Python libraries that the notebook depends on.
- [DATA](DATA) : contains all data sets and further ressources that are used within the Jupyter Notebook.

## Usage

Dependencies are specified in [requirements.txt](/requirements.txt) :

```
pip install -r requirements.txt
```

You can access this repo via **Binder** at the following URL 
https://mybinder.org/v2/gh/tbsv/ML_decision-tree/master or via the Binder badge above.

Alternatively, you can run the notebook locally. Therefore, you will need to have python installed,
preferably through [Anaconda](https://www.anaconda.com/download/).

## Run the notebook

Each cell of code can be run with `shift + enter` or you can run the entire notebook by selecting `Cell` -> `Run All` in the toolbar.

![Screenshot](DATA/jn_run-all.png?raw=true "Screenshot")

For more information on running Jupyter notebooks, see the [Jupyter Documentation](https://jupyter.readthedocs.io/en/latest/).

## Example (for reproduction)

### Import libraries
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
%matplotlib inline
```

### Import data set
```python
loans = pd.read_csv('./DATA/loan_data.csv')
```

### Create a countplot with seaborn, where the number of loans are in relation to the purpose. Hue should be defined in the column "not.fully.paid"
```python
plt.figure(figsize=(11,7))
sns.countplot(x='purpose',hue='not.fully.paid',data=loans,palette='Set1')
```

### Result plot
![plot](DATA/decision-tree_countplot.png?raw=true "Plot")

## Issues

Please [open an issue](https://github.com/tbsv/ML_logistic-regression/issues) if you encounter any problems while trying to run the notebooks.

## About
This data science exercise is part of the Digital Business Engineering Master at HHZ.

The given example was taken from the Udemy course [Python for Data Science, Machine Learning & Visualization](https://www.udemy.com/course/python-data-science-machine-learning/).

Adaptions to the jupyter notebook are made by [Tobias Vetter](mailto:tobias.vetter@student.reutlingen-university.de).