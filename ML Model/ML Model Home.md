---
type: home
project: ML Model
status: done
started: 2026-09-20
repo: https://github.com/TheAnakin01/Regular_ML-Model
tags: [ml-model, home, machine-learning, python]
---
# 🤖 ML Model — Home

Back to [[Projects]]

My first machine-learning project: predict how well a molecule **dissolves in water** (`logS`) from 4 simple chemistry
numbers, then compare two models. One Jupyter notebook (`SMLD_ML_Project.ipynb`) that runs in Google Colab.

## 🔗 Links
- **Code:** https://github.com/TheAnakin01/Regular_ML-Model
- **Open in Colab:** https://colab.research.google.com/github/TheAnakin01/Regular_ML-Model/blob/main/SMLD_ML_Project.ipynb

## 📦 Data
Delaney solubility dataset: **1,144 molecules** (from the `dataprofessor/data` GitHub repo).

| Column | Meaning | Role |
|---|---|---|
| `MolLogP` | How oily vs watery the molecule is | input (X) |
| `MolWt` | Molecular weight | input (X) |
| `NumRotatableBonds` | How flexible the molecule is | input (X) |
| `AromaticProportion` | Share of atoms in aromatic rings | input (X) |
| `logS` | Solubility | **target (y)** |

## 🧪 Steps
1. Load CSV with **pandas**
2. Split into `X` (4 inputs) and `y` (`logS`)
3. `train_test_split`: 80% train / 20% test, `random_state=100`
4. Train **Linear Regression** and **Random Forest** (`max_depth=2`) with scikit-learn
5. Score both with **MSE** (lower = better) and **R²** (closer to 1 = better)
6. Scatter plot of predicted vs actual with matplotlib

## 📊 Results
| Model | Train MSE | Train R² | Test MSE | Test R² |
|---|---|---|---|---|
| **Linear Regression** 🏆 | 1.008 | 0.765 | **1.021** | **0.789** |
| Random Forest (depth 2) | 1.028 | 0.760 | 1.408 | 0.709 |

**Winner: Linear Regression.** The Random Forest was limited to `max_depth=2` (only 4 leaves), so it was too
simple to beat a straight line.

## 💡 Ideas for v2
- Try Random Forest with a larger `max_depth` (or the default) and compare again
- Add the plot for **test** predictions, not just training
- Write a short README in the repo explaining the project (it's currently just a title)
