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
from pandas.plotting import scatter_matrix
```

```python
# remove irrelevant variables
data = pd.read_csv('train.csv')
data = data.drop("Id", axis=1)
attributes = ["SalePrice","OverallQual", "GrLivArea", "GarageCars", "GarageArea", "TotalBsmtSF"]
scatter_matrix(data[attributes], figsize=(70, 70))
```

```python
#
```

```python

```
