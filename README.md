# Spotter Freight Rate Prediction

## Approach Overview
* **Algorithm:** Gradient Boosting Regressor (`xgboost`).
* **Feature Engineering:** Extracted temporal features (`dayofweek`, `month`, `days_since_start`) to capture seasonal trends. Handled unseen validation categories dynamically to prevent pipeline failures.
* **Validation:** Implemented an 85/15 chronological out-of-time split to prevent temporal data leakage.

## Run Instructions
1. Install dependencies: `pip install -r requirements.txt`
2. Run pipeline: `python main.py`
3. Score: `python score.py --predictions validation_predictions.csv --december-predictions december-chart-inputs.csv`
