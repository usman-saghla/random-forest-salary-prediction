# Random Forest Regression

This small project demonstrates Random Forest Regression on the `Position_Salaries.csv` dataset and includes a higher-resolution visualization plus an advanced plot that shows per-tree predictions and an uncertainty band.

## Contents

- `Position_Salaries.csv` — dataset used in the notebook
- `random_forest_regression.ipynb` — Jupyter notebook with model training, prediction, and two visualizations:
  - high-resolution prediction plot
  - per-tree variability + ±1 std dev uncertainty band (advanced)
- `requirements.txt` — Python dependencies for quick setup

## What the notebook shows

- Training a RandomForestRegressor on the full dataset.
- Predicting a single value (e.g., level 6.5).
- A higher-resolution static plot (fine-grained grid) of the RF prediction.
- An advanced visualization that plots every individual tree's prediction (light gray lines), the ensemble mean (solid blue), and a shaded ±1 standard-deviation band to illustrate model variability/uncertainty.

## Notes

- A small code fix was applied to avoid a DeprecationWarning from NumPy 1.25+: the grid now uses `X.min()` / `X.max()` instead of Python's built-in `min(X)` / `max(X)` on a numpy array.
- If you want interactive exploration (hover, toggle tree lines), consider converting the advanced plot to Plotly—happy to add an interactive cell.

## Next steps / optional improvements

- Add a `requirements.txt` (included) and optionally pin versions.
- Add an interactive Plotly visualization so you can toggle visibility of individual trees.
- Compute empirical prediction intervals (e.g., 2.5% / 97.5% percentiles) from `all_preds` and display them in the notebook.

---

If you'd like, I can convert the advanced static plot to an interactive Plotly figure and add that cell to the notebook, or run the notebook and confirm there are no runtime warnings/errors.
