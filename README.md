# Recourse Analysis Notebook

This notebook demonstrates a comprehensive analysis of algorithmic recourse using a machine failure prediction dataset. It covers data loading, preprocessing, model training (Logistic Regression and LightGBM), model calibration, and various recourse strategies.

## Sections

1.  **Data Loading and Initial Exploration**: Loads the dataset and identifies potential label and ID columns.
2.  **Handling Label Inconsistencies**: Detects and addresses inconsistencies between the 'Machine failure' label and the failure mode flags.
3.  **Model Training and Evaluation (Logistic Regression)**: Trains a Logistic Regression model, calibrates it, and evaluates its performance using AUROC and AUPRC.
4.  **Recourse for Logistic Regression**: Implements and evaluates bounded L1-penalized recourse for the Logistic Regression model.
5.  **Sparsity Sweep**: Analyzes the trade-off between L1 penalty and the number of features changed in recourse.
6.  **Sensitivity Study**: Explores the impact of the safety threshold (τ_safe) and maximum percentage change budget on recourse outcomes.
7.  **Stability Analysis**: Assesses the stability of recourse results across different random seeds and train/test splits.
8.  **LightGBM Baseline and Recourse**: Trains a LightGBM model, calibrates it, and applies local linear surrogate recourse.
9.  **Model Comparison**: Compares the performance and recourse characteristics of the Logistic Regression and LightGBM models.
10. **K-sparse Recourse**: Implements and evaluates recourse constrained to change exactly *k* features.
11. **Visualization Pack**: Generates key plots summarizing the analysis.

## How to Use

Run the cells sequentially. Ensure the dataset `ai4i2020.csv` is available in the specified path. You can modify parameters like `tau_safe`, `max_pct_change`, and `l1_weight` in the relevant cells to explore different recourse settings.

## Outputs

The notebook generates several CSV files containing detailed results from the recourse analysis, which can be downloaded for further inspection. Key plots are also generated and saved as PNG files.
