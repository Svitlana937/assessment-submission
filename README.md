# Applied Statistics: Exploring the Iris Dataset

This project explores the classic Iris flower dataset using Python, pandas,
Seaborn, Matplotlib, NumPy, and SciPy. The accompanying notebook analyzes petal
length distributions and the relationship between petal length and petal width.

## Project goals

- Load and export the Iris dataset.
- Compare petal-length distributions for all flowers and for each species.
- Calculate and interpret descriptive statistics.
- Measure the correlation between petal length and petal width.
- Visualize distributions and linear relationships.

## Dataset

The data contains 150 observations: 50 each of **setosa**, **versicolor**, and
**virginica**. It includes four numeric measurements:

| Column | Description |
| --- | --- |
| `sepal_length` | Sepal length in centimeters |
| `sepal_width` | Sepal width in centimeters |
| `petal_length` | Petal length in centimeters |
| `petal_width` | Petal width in centimeters |
| `species` | Iris species |

The notebook loads the dataset through `seaborn.load_dataset('iris')` and exports
a local copy to `data/iris.csv`.

## Getting started

### 1. Create and activate a virtual environment

```bash
python -m venv .venv
source .venv/bin/activate
```

### 2. Install the dependencies

```bash
python -m pip install -r requirements.txt
```

### 3. Open the notebook

```bash
jupyter notebook problems.ipynb
```

## Notebook overview

### Problem 1: Exploring petal length

The notebook plots petal-length histograms, calculates the overall mean and
standard deviation, overlays a normal distribution, and repeats the distribution
analysis separately for each species.

For petal length across the full dataset:

- Mean: approximately 3.758 cm
- Standard deviation: approximately 1.765 cm
- Setosa mean: 1.462 cm
- Versicolor mean: 4.260 cm
- Virginica mean: 5.552 cm

Setosa has the smallest, least variable petal lengths, while virginica has the
largest average petal length. These differences provide a clear starting point
for separating the species using petal measurements.

### Problem 2: Correlation between petal length and petal width

Pearson's correlation coefficient measures the strength and direction of a linear
relationship. A value near 1 indicates a strong positive relationship.

- All flowers: **r = 0.963**
- Setosa: **r = 0.332**
- Versicolor: **r = 0.787**
- Virginica: **r = 0.322**

Across all species, petal length and petal width have a strong positive
correlation. Within each species, the correlation is weaker and varies; the
strong overall result is influenced by the difference in sizes between species.

## Repository files

- `problems.ipynb` — analysis, plots, calculations, and interpretations
- `data/iris.csv` — local CSV export of the Iris dataset
- `iris_dataset.csv` — additional CSV copy of the dataset
- `requirements.txt` — Python package dependencies
- `README.md` — project documentation
