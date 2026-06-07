# Stochastic Interest Rate Modelling and Prediction

This project investigates the reconstruction and forecasting of the U.S. Treasury yield curve using the Cox-Ingersoll-Ross (CIR) short-rate model and its multi-factor extensions. Starting from a classical single-factor CIR framework, the study develops two-factor and three-factor affine term structure models to improve out-of-sample predictive performance using only the 3-month Treasury yield as an observable input during testing.

The final three-factor model achieved an out-of-sample coefficient of determination of approximately **R² = 0.887**, exceeding the target benchmark of **R² > 0.85**.

---

## Repository Structure

### Main Notebook

* `25123016_Keval_Mandalia_Finance_Club_IITR_Open_Project_2026_Stochastic_Interest_Rate_Modelling_and_Prediction.ipynb`

  Complete implementation of:

  * Single-Factor CIR Model
  * Two-Factor Level-Slope Extension
  * Three-Factor Affine Extension
  * Calibration
  * Yield Curve Reconstruction
  * Out-of-Sample Evaluation
  * Visualization and Performance Analysis

---

## Datasets

### Training Data

* `train_data.csv`

  Historical Treasury yield data used for model calibration and parameter estimation.

### Test Inputs

* `test_data_3M.csv`

  Contains only the 3-month Treasury yield used as the observable input during out-of-sample forecasting.

### Test Targets

* `test_data.csv`

  Contains the full yield curve and is used only for model evaluation and performance measurement.

---

## Model Predictions

### Base CIR Model

* `pred_data_base-model.csv`

  Predicted yield curve generated using the single-factor CIR framework.

### Two-Factor Level-Slope Model

* `pred_data_two_factor.csv`

  Predicted yield curve generated using the two-factor extension with:

  * Level Factor: 3M Yield
  * Slope Factor: 2Y − 3M Spread

### Three-Factor Affine Model

* `pred_data_3factor.csv`

  Predicted yield curve generated using:

  * Level Factor: 3M Yield
  * Medium-Term Slope Factor: 1Y − 3M Spread
  * Long-End Slope Factor: 2Y − 1Y Spread

---

## Model Performance

| Model                         | Combined Out-of-Sample R² |
| ----------------------------- | ------------------------: |
| Single-Factor CIR             |                     0.718 |
| Two-Factor Level-Slope        |                     0.822 |
| Three-Factor Affine Extension |                     0.887 |

---

## Key Result

The results demonstrate that while the classical CIR model provides a useful foundation for yield curve modeling, additional factors are required to accurately capture the dynamics of the term structure. The three-factor affine extension provides the best overall performance and significantly improves yield curve reconstruction accuracy across maturities.

---

## Author

Keval Mandalia,

Enrollment no. : 25123016,

BTech. Electrical Engineering,

Department of Electrical Engineering,

Indian Institute of Technology Roorkee (IIT Roorkee).
