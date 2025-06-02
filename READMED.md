# Solar Plant Performance Analysis

## Overview

This repository contains a comprehensive analysis of solar plant performance data, focusing on the relationship between Performance Ratio (PR) and Global Horizontal Irradiance (GHI). The analysis helps identify patterns, seasonal variations, and anomalies in solar plant performance to optimize energy production and maintenance scheduling.

## Key Insights

- Performance Ratio shows a moderate correlation with GHI values
- Distinct seasonal patterns identified in both PR and GHI metrics
- Statistical anomaly detection reveals potential maintenance issues
- Higher GHI days (>4 kWh/m²) generally show more stable PR values
- Monthly performance heatmaps highlight year-over-year efficiency changes

## Installation

```bash
# Clone the repository
git clone https://github.com/Dhruv-413/solar-data-analysis.git
cd solar-data-analysis

# Create and activate virtual environment
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter notebook
jupyter notebook
```

## Data Description

The analysis uses two primary datasets spanning July 2019 to March 2022:

1. **GHI Data**: Daily Global Horizontal Irradiance measurements (kWh/m²)
2. **PR Data**: Daily Performance Ratio values (%)

## Analysis Components

### 1. Data Preprocessing
- Data loading and consolidation from multiple CSV files
- Cleaning and normalization of GHI and PR metrics
- Merging datasets on date keys with quality verification

### 2. PR-GHI Relationship Analysis
- Statistical correlation between PR and GHI values
- Regression modeling to establish expected performance baselines
- Binned analysis of PR performance across GHI ranges

### 3. Temporal Analysis
- Time series visualization with 30-day moving averages
- Budget PR comparison with degradation modeling
- Year-over-year and month-over-month performance comparisons

### 4. Anomaly Detection
- Statistical outlier identification using regression residuals
- Visual highlighting of performance anomalies
- Quantification of deviation from expected performance

### 5. Seasonal Pattern Detection
- Monthly performance averages and distributions
- Seasonal grouping and statistical analysis
- Heatmap visualizations for pattern identification

## Key Visualizations

The notebook generates several insightful visualizations saved to the `output/` directory:

- **PR Time Series**: Performance tracking with moving averages and budget lines
- **PR-GHI Scatter**: Relationship between PR and GHI with regression models
- **Monthly Heatmaps**: PR and GHI patterns visualized by month and year
- **Anomaly Detection**: Visual identification of performance outliers
- **Seasonal Distributions**: PR and GHI distributions across different seasons

## Code Structure

The main analysis is contained in the Jupyter notebook `solar_data_analysis.ipynb` with the following key functions:

- `preprocess_solar_data()`: Data loading and preparation
- `plot_pr_graph()`: Time series visualization of Performance Ratio
- `analyze_pr_ghi_relationship()`: Statistical analysis of PR-GHI correlation
- `analyze_seasonal_patterns()`: Temporal pattern identification
- `detect_anomalies()`: Statistical anomaly detection
- `analyze_monthly_ghi()`: Monthly GHI pattern analysis
- `summarize_performance()`: Performance metrics summary

## Results and Applications

This analysis provides actionable insights for:

- Optimizing maintenance schedules based on seasonal patterns
- Setting realistic performance expectations across varying irradiance conditions
- Identifying underperforming periods requiring investigation
- Establishing data-driven performance baselines for future plants
- Quantifying the relationship between irradiance and performance

## Dependencies

- pandas: Data manipulation and analysis
- matplotlib/seaborn: Data visualization
- scikit-learn: Machine learning for regression and anomaly detection
- scipy: Statistical analysis
- numpy: Numerical computations
