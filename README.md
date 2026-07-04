# Sales Forecasting with LSTM and W&B

This project demonstrates a complete workflow for time series sales forecasting using an LSTM neural network in PyTorch, with experiment tracking and artifact management via Weights & Biases (W&B). The workflow is implemented in a Jupyter notebook and covers data ingestion, preprocessing, model training, and evaluation.

## Project Overview

- **Data Source:** UCI Online Retail dataset ([link](https://archive.ics.uci.edu/ml/machine-learning-databases/00352/Online%20Retail.xlsx))
- **Frameworks:** PyTorch, scikit-learn, pandas, matplotlib
- **Experiment Tracking:** Weights & Biases (W&B)
- **Model:** LSTM for univariate time series forecasting

## Workflow

1. **Data Ingestion:**
   - Downloads the raw sales data and logs it as a W&B artifact.
2. **Data Preprocessing:**
   - Cleans the data, aggregates daily sales, splits into training and validation sets, and logs processed artifacts.
3. **Model Training:**
   - Trains an LSTM model on the processed data, tracks metrics, and logs the best model to W&B.
4. **Evaluation:**
   - Loads the best model from the W&B model registry, generates forecasts, and logs performance metrics and plots.

## Getting Started

### Prerequisites

- Python 3.8+
- Jupyter Notebook
- [Weights & Biases account](https://wandb.ai/)

Note: Preferred environment for quick setup: Google Colab

### Installation

Install required packages (or run cell 1 in Colab):

```bash
pip install wandb==0.21.1 scikit-learn==1.6.1 torch==2.6.0+cu124 pandas numpy matplotlib
```

### W&B Setup

Log in to W&B (cell 2) before running the notebook:

```bash
wandb login
```

## Usage

1. Open `notebook.ipynb` in Jupyter/Google Colab.
2. Run all cells sequentially:
   - Data ingestion and preprocessing will download and clean the dataset.
   - The LSTM model will be trained and the best model logged to W&B.
   - Evaluation will load the best model and log forecast results.

## Project Structure

- `notebook.ipynb` — Main notebook containing the full workflow
- `README.md` — Project documentation

## Notes

- All experiment runs, datasets, and models are tracked and versioned in W&B.
- The notebook is modular, with each step (ingestion, preprocessing, training, evaluation) clearly separated.

Thank you!!
