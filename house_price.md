---
jupyter:
  jupytext:
    formats: ipynb,md
    text_representation:
      extension: .md
      format_name: markdown
      format_version: '1.3'
      jupytext_version: 1.16.4
  kernelspec:
    display_name: Python 3 (ipykernel)
    language: python
    name: python3
---

```python
import pandas as pd
```

```python
data = pd.read_csv('train.csv')
```

```python
from pandas.plotting import scatter_matrix
# remove irrelevant variables
data = data.drop("Id", axis=1)
# create the test set
from sklearn.model_selection import train_test_split
train_data, test_data = train_test_split(data, test_size=0.2, random_state=42)
# compute the standard correlation coefficient
housing = train_data.copy()
attributes = ["SalePrice","OverallQual", "GrLivArea", "GarageCars", "GarageArea"]
scatter_matrix(housing[attributes], figsize=(12, 12))
```

```python

```
