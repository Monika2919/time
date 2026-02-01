# time

Time Series Forecasting: Dense Baseline vs LSTM with Attention

README
Dense Baseline vs LSTM with Attention – Time Series Forecasting
Overview

This project compares a Dense (feed-forward) baseline model and an LSTM model with attention for univariate time series forecasting, with the objective of evaluating whether increased model complexity improves prediction accuracy.

Files

Untitled1.ipynb – Complete runnable Python implementation, including preprocessing, model training, evaluation, and visualizations.

Dataset & Preprocessing

A synthetic time series with trend, seasonality, and noise is used.
Preprocessing includes Min-Max scaling, a 30-step look-back window, and an 80/20 chronological train–test split.

Models

Dense Baseline: Flattened input followed by Dense layers

LSTM with Attention: LSTM layer with self-attention for temporal weighting

Hyperparameter Tuning

Hyperparameters were tuned using a manual grid search, minimizing validation MSE. Early stopping was applied to improve generalization.

Evaluation Results
Metric	Dense	Attention LSTM
RMSE	0.55	1.77
MAE	0.44	1.53
MAPE	3.24%	10.89%
Visualizations

The notebook includes actual vs. predicted plots on the test set for both models.

Conclusion

The Dense baseline model consistently outperformed the LSTM with attention across all evaluation metrics. This suggests that for time series with smooth and regular patterns, simpler models can generalize better than more complex architectures. The results highlight the importance of aligning model complexity with data characteristics rather than assuming that advanced models will always yield superior performance.
