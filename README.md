# Applied Statistics: Exploring the Iris Dataset

This project is a small data-analysis starter based on the classic Iris flower dataset. The repository currently contains a few initial notebook cells and supporting files, with more analysis to be added later.

## Project goal

Explore how petal and sepal measurements vary across the three Iris species and build a simple statistical workflow around the dataset.

## Starter notebook cells

### Cell 1: imports

```python
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
from scipy import stats
```

### Cell 2: load the data

```python
iris_df = sns.load_dataset('iris')
iris_df.head()
```

### Cell 3: basic summary

```python
iris_df.describe()
```

### Cell 4: quick visualization

```python
sns.scatterplot(data=iris_df, x='petal_length', y='petal_width', hue='species')
plt.title('Iris petal dimensions by species')
plt.show()
```

## Files in this repo

- `problems.ipynb` — working notebook with the analysis
- `data/iris.csv` — exported dataset used in the project
- `requirements.txt` — package requirements

This README is intentionally a starting point. We will expand it as the notebook grows.
