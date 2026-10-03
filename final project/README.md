# Power Output Estimator

Final project for **ENGR 1330 – Computational Thinking and Data Science**. The project estimates the net electrical power output of a combined-cycle power plant from ambient operating conditions.

## Overview

The notebook explores the UCI Combined Cycle Power Plant dataset, which contains hourly observations from 2006–2011. It explains the operating principles of combined-cycle plants, examines the data, trains an ordinary least-squares linear regression model, evaluates the model on a held-out test set, and provides a reusable prediction function with an approximate uncertainty interval.

The model uses four inputs:

- `AT` — ambient temperature (°C)
- `V` — exhaust vacuum (cm Hg)
- `AP` — ambient pressure (mbar)
- `RH` — relative humidity (%)

It predicts `PE`, the net hourly electrical power output (MW).

## Contents

- `Power output predictor project.ipynb` — complete analysis, visualizations, regression model, diagnostics, and scenario predictions.

## Running the project

1. Install Python packages: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, and Jupyter.
2. Download the Combined Cycle Power Plant dataset from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/294/combined+cycle+power+plant) and place `ccpp.csv` in this folder.
3. Open the notebook and select **Kernel → Restart & Run All**.

The notebook performs an 80/20 train/test split with `random_state=42`, reports RMSE, MAE, and R², and defines `predict_power(AT, V, AP, RH)` for estimating power output.

## Authors

Sander Garita, Alexandra Schäffer, and Diana Rodriguez.