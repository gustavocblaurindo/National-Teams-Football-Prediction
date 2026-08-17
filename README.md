# Prediction System for National Football Team Match Results

This repository contains the Jupyter Notebook and the final processed dataset used in the experiments reported in the paper **"Prediction System for National Football Team Match Results"** (ENIAC 2026).

## Contents

- **`ClassificationFootball.ipynb`**: Elo rating computation, feature engineering, model training (XGBoost, Logistic Regression, MLP Neural Network), and evaluation under Rolling Window and Expanding Window temporal validation.
- **`FinalDataset.csv`** — final dataset resulting from the feature engineering process described in the paper, ready to reproduce the experiments directly (matches from 2015 onward, enriched with Elo ratings, recent-performance indicators, and aggregated FIFA player ratings).

## Original raw data sources

The raw data used to build `FinalDataset.csv` are not included in this repository to avoid redundancy, since they are large third-party datasets already hosted on Kaggle. The original sources (also referenced inside the notebook) are:

1. **International match results (1872–2017):**
   https://www.kaggle.com/datasets/martj42/international-football-results-from-1872-to-2017
2. **FIFA World Cup history:**
   https://www.kaggle.com/datasets/abhijitdahatonde/fifa-world-cup-all-dataset
3. **FIFA player ratings (FIFA 15 to FIFA 24):**
   https://www.kaggle.com/datasets/joebeachcapital/fifa-players
4. **EA Sports FC 25 player ratings:**
   https://www.kaggle.com/datasets/nyagami/ea-sports-fc-25-database-ratings-and-stats
5. **EA Sports FC 26 player ratings:**
   https://www.kaggle.com/datasets/rovnez/fc-26-fifa-26-player-data

These sources are only needed if you want to rebuild `FinalDataset.csv` from scratch. To reproduce the experiments and results reported in the paper, `FinalDataset.csv` alone is sufficient.

## How to reproduce the experiments

1. Clone this repository.
2. Install the required Python packages (Scikit-learn, XGBoost, Pandas, NumPy, Matplotlib, Seaborn).
3. Open `ClassificationFootball.ipynb` and run the cells starting from the supervised learning section, using `FinalDataset.csv` as the input file.
