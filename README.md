# RFF-HBO-TSF

## Project Overview

RFF-HBO-TSF (Random Fourier Features - Hyperparameter Bayesian Optimization - Time Series Forecasting) is a comprehensive research project focused on time series forecasting using advanced machine learning techniques. The project implements and evaluates various recurrent neural network architectures (RNN, LSTM, GRU) with Random Fourier Features for time series prediction across multiple datasets.

## Project Structure

```
RFF-HBO-TSF/
├── Data/                                    # Dataset storage and results
│   ├── DS1_1440.csv                        # Dataset 1 with 1440 samples
│   ├── DS2_1448.csv                        # Dataset 2 with 1448 samples
│   ├── data_dict.pkl                       # Processed data dictionary
│   ├── results_by_series.pkl               # Forecasting results by time series
│   ├── extracted_hyperparameters_summary.csv # Summary of hyperparameter optimization
│   ├── UMAPCDDA/                           # UMAP and CDDA datasets
│   │   ├── Argone_IL.txt
│   │   ├── Beijing_Airport_China.txt
│   │   └── Chengdu_Airport_China.txt
│   ├── Using Fusion Models for Forecasting of Wind Speed and Direction/
│   │   └── dataset.pkl
│   └── Wind_data_NL/                       # Netherlands wind data
│       ├── dataset.pkl
│       └── scaler.pkl
├── RFF-HBO-RSF_search/                     # Hyperparameter optimization results
│   ├── Beijing/                            # Beijing airport dataset results
│   ├── Chengdu/                            # Chengdu airport dataset results
│   ├── Ethiopia-Argone/                    # Ethiopia and Argone datasets
│   ├── Lorenz/                             # Lorenz attractor dataset
│   ├── Netherlands_0/                      # Netherlands dataset 0
│   ├── Netherlands_1/                      # Netherlands dataset 1
│   └── Netherlands_2/                      # Netherlands dataset 2
├── Figures/                                # Generated plots and visualizations
│   ├── eps/                                # EPS format figures
│   │   ├── lorenz_all_metrics.eps
│   │   ├── worldwide_mae_heatmap.eps
│   │   ├── worldwide_mape_heatmap.eps
│   │   └── worldwide_r2_heatmap.eps
│   └── Reconstruction/                     # Time series reconstruction plots
│       ├── Argone_h1_t0-100.eps
│       ├── resultados_forecasting_6.eps
│       └── resultados_forecasting.eps
├── Jupyter Notebooks/
│   ├── HyperParameters.ipynb               # Hyperparameter analysis
│   ├── Organize_Datasets.ipynb             # Dataset organization and preprocessing
│   ├── Results.ipynb                       # Results analysis and visualization
│   └── Statistical_Analysis.ipynb          # Statistical analysis of results
├── Python Scripts/
│   ├── extract_hyperparameters.py          # Extract and organize hyperparameters
│   ├── plot_reconstruction_updated.py      # Plot time series reconstructions
│   ├── run_reconstruction_plot.py          # Execute reconstruction plotting
│   └── test_reconstruction_configs.py      # Test reconstruction configurations
└── venv/                                   # Python virtual environment
```

## Key Components

### 1. Datasets
The project includes multiple time series datasets:
- **Airport Data**: Beijing and Chengdu airport time series
- **Wind Data**: Netherlands wind speed and direction data
- **Lorenz Attractor**: Synthetic chaotic time series
- **Ethiopia Data**: Environmental time series from Ethiopia
- **Argone Data**: Scientific measurement data

### 2. Hyperparameter Optimization
The `RFF-HBO-RSF_search/` directory contains results from Bayesian hyperparameter optimization using Optuna for different RNN architectures:
- **RNN Types**: RNN, LSTM, GRU, and NoRNN (baseline)
- **Optimization Metrics**: R² score, MAE, MAPE
- **Hyperparameters**: Kernel size, number of features (NF), learning rate, etc.

### 3. Analysis Tools
- **Hyperparameter Extraction**: Automated extraction and analysis of optimization results
- **Reconstruction Visualization**: Tools for plotting time series reconstructions
- **Statistical Analysis**: Comprehensive statistical evaluation of model performance

### 4. Results and Visualizations
- **Performance Metrics**: Heatmaps and comparative analysis across datasets
- **Time Series Reconstruction**: Visual comparison of predicted vs actual values
- **Statistical Plots**: Distribution analysis and model comparison

## Usage

### Environment Setup
```bash
# Activate virtual environment
source venv/bin/activate

# Install dependencies (if needed)
pip install -r requirements.txt
```

### Running Analysis
1. **Extract Hyperparameters**:
   ```bash
   python extract_hyperparameters.py
   ```

2. **Generate Reconstruction Plots**:
   ```bash
   python run_reconstruction_plot.py
   ```

3. **Interactive Analysis**:
   - Open Jupyter notebooks for detailed analysis
   - Use `HyperParameters.ipynb` for hyperparameter analysis
   - Use `Results.ipynb` for comprehensive results evaluation

## Research Focus

This project investigates:
- **Random Fourier Features** for time series forecasting
- **Bayesian Hyperparameter Optimization** for neural network tuning
- **Recurrent Neural Network Architectures** (RNN, LSTM, GRU) comparison
- **Multi-dataset Performance Evaluation** across diverse time series

## Output Files

- **Hyperparameter Summaries**: CSV files with optimization results
- **Reconstruction Plots**: EPS format visualizations of time series predictions
- **Statistical Analysis**: Comprehensive performance metrics and comparisons
- **Processed Data**: Pickle files with preprocessed datasets and results

## Dependencies

The project uses Python with key libraries including:
- NumPy, Pandas for data manipulation
- Matplotlib, Seaborn for visualization
- Optuna for hyperparameter optimization
- PyTorch/TensorFlow for neural network implementation
- Jupyter for interactive analysis

## License

[Add license information here]

## Contact

[Add contact information here]
