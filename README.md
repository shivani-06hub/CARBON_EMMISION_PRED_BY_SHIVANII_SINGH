# CARBON_EMMISION_PRED_BY_SHIVANII_SINGH

This project aims to forecast carbon dioxide (CO₂) emissions using a comprehensive dataset that includes demographic, economic, land-use, and energy consumption indicators. By applying machine learning—specifically the Random Forest Regressor—we build a predictive model that can estimate future greenhouse gas (GHG) emissions with high accuracy. This tool is intended to support environmental policy planning and sustainability research.

# THE MODEL IS ALSO ATTACHED IN THE RELEASE SECTION YOU CAN DOWNLOAD IT FROM THERE ALSO!!
🔗 **Model Access**: [Download the trained model](https://drive.google.com/file/d/1E7ku6arbCqdKQWGQFme5bxlPK8asC1Jt/view?usp=sharing)

## Required Libraries
Install the following dependencies before running the project:
pip install numpy pandas seaborn streamlit matplotlib scikit-learn

## Project Workflow

### 1. Data Preparation

This phase ensures the dataset is clean, consistent, and ready for modeling:

- **Data Acquisition**:
  - Aggregated from multiple sources including global CO₂ datasets, World Bank indicators, and energy statistics.
- **Cleaning & Preprocessing**:
  - Handling missing values using imputation (mean/median).
  - Removing duplicates and irrelevant columns.
  - Standardizing units and formats.
- **Feature Engineering**:
  - Creating derived metrics such as CO₂ per capita, energy intensity, and GDP-to-emission ratios.
  - Encoding categorical variables (e.g., countries) using one-hot encoding.
- **Scaling**:
  - Applying normalization (MinMaxScaler) to ensure uniform feature distribution.

### 2.  Exploratory Data Analysis (EDA)

EDA helps uncover patterns, correlations, and anomalies in the dataset:

- **Univariate Analysis**:
  - Histograms and KDE plots for variables like CO₂ emissions, GDP, and population.
- **Multivariate Analysis**:
  - Correlation heatmaps to identify strong predictors.
  - Pair plots to visualize feature interactions.
- **Outlier Detection**:
  - Box plots and IQR-based filtering to manage extreme values.
- **Temporal & Geospatial Trends**:
  - Line plots to observe emission trends over time.
  - Choropleth maps to visualize emissions by country.

### 3.  Model Building & Prediction (Random Forest Regressor)

The predictive model is built using the Random Forest algorithm, chosen for its robustness and ability to handle non-linear relationships:

- **Train-Test Split**:
  - Dataset split into training and testing sets (typically 80/20).
- **Model Selection**:
  - Random Forest Regressor selected for its ensemble learning capability and resistance to overfitting.
- **Training**:
  - Model trained on the prepared dataset using default and tuned hyperparameters.
- **Hyperparameter Tuning**:
  - GridSearchCV used to optimize parameters such as:
    - `n_estimators` (number of trees)
    - `max_depth`
    - `min_samples_split`
    - `min_samples_leaf`
- **Evaluation Metrics**:
  - R² Score
  - Mean Absolute Error (MAE)
  - Root Mean Squared Error (RMSE)
- **Prediction & Visualization**:
  - Forecasted CO₂ emissions plotted against actual values.
  - Residual plots used to assess model bias and variance.

##  Future Enhancements

- Integration with real-time data APIs for live forecasting.
- Deployment of an interactive Streamlit dashboard.
- Incorporation of deep learning models (e.g., LSTM for time-series forecasting).
- Scenario modeling for policy simulations (e.g., carbon tax, renewable energy adoption).
