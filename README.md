# Predicting Electric Vehicle Charging Loads with PyTorch

This project uses PyTorch to predict residential electric vehicle charging loads using real-world data from apartment buildings in Norway.

The project began as a Codecademy PyTorch portfolio exercise and is being extended with additional validation, preprocessing, model comparison, diagnostics, and reproducibility steps.

## Objective

The target variable is `El_kWh`, the electrical energy consumed during a charging session.

Potential predictors include:

- plug-in duration
- charging location characteristics
- month
- day of the week
- local traffic density
- other numerical charging-session features

The main modelling question is:

> Can a feed-forward neural network predict EV charging load better than a simple linear-regression baseline?

## Dataset

Source:

https://data.mendeley.com/datasets/jbks2rcwyj/1

Raw datasets are not stored in this repository.

## Planned workflow

1. Load and inspect the charging and traffic datasets.
2. Merge charging sessions with traffic information.
3. Clean and prepare numerical features.
4. Define predictors and the `El_kWh` target.
5. Split data into training, validation, and test sets.
6. Fit a linear-regression baseline.
7. Standardise input features.
8. Build a PyTorch feed-forward neural network.
9. Train while monitoring training and validation loss.
10. Evaluate on held-out test data.
11. Compare linear regression and neural-network performance.
12. Visualise predicted versus observed values.
13. Inspect residuals and prediction errors.
14. Test whether traffic information improves prediction.
15. Save trained model weights reproducibly.

## Initial neural-network architecture

Input features
↓
Linear(input_features → 56)
↓
ReLU
↓
Linear(56 → 26)
↓
ReLU
↓
Linear(26 → 1)
↓
Predicted charging load

## Evaluation

The final analysis will report:

- MSE
- RMSE
- MAE
- training and validation loss curves
- predicted-versus-observed plots
- residual diagnostics

## Attribution

The starting project specification is based on Codecademy's PyTorch learning material.

The implementation, extensions, model comparisons, diagnostics, and interpretation are being developed as an independent portfolio project.

## Status

Work in progress.
