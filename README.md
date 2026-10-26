# Predicting Stellar Class

Kaggle Playground Series S6E6 (`playground-series-s6e6`): classify objects as `GALAXY`, `STAR` or `QSO` from photometric magnitudes (`u`, `g`, `r`, `i`, `z`), position, redshift, and two categorical columns. Metric: balanced accuracy.

## Approach

1. EDA of features, class balance and correlations.
2. Feature engineering: colour indices (`u-g`, `g-r`, `r-i`, `i-z`) replace the raw bands.
3. Random forest baseline.
4. XGBoost random search, coarse then fine (3-fold then 5-fold CV).
5. Final ensemble of top XGBoost configurations (weighted blend and stacker).

Best XGBoost CV balanced accuracy: about 0.9475.

## Files

| File | Purpose |
|---|---|
| `01_eda.ipynb` | Exploratory data analysis |
| `02_baseline_rf.ipynb` | Random forest baseline |
| `03_coarse_search.ipynb` | Coarse XGBoost random search |
| `04_fine_search.ipynb` | Fine search around the best coarse configs |
| `05_final_ensemble.ipynb` | Final ensemble and submission |
| `xgb_course_random_search_results.csv` | Coarse search trial results |
| `xgb_fine_random_search_results.csv` | Fine search trial results |
