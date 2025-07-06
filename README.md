 # Power-Pulse-Household-Energy-Usage-Forecast
PowerPulse is a data-driven project that forecasts household energy consumption using time series and machine learning. It analyzes the UCI Household Power Consumption dataset to identify usage patterns and build predictive models, helping users and energy providers make informed, efficient decisions about energy use.
---

## 📌 Project Objectives

- Accurately predict household power consumption using ML models.
- Identify key factors influencing energy usage.
- Visualize time-based consumption patterns and model performance.

---

## 🗃️ Dataset Details

- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/235/individual+household+electric+power+consumption)
- **File**: `individual+household+electric+power+consumption.zip`
- **Frequency**: 1-minute intervals
- **Period**: Dec 2006 and November 2010 (47 months)
- **Domain**: Energy & Utilities

---

## 🧹 Data Preparation

- Converted necessary columns to numeric with `pd.to_numeric()`.
- Imputed missing values using median strategy.
- Dropped highly correlated feature (`Global_intensity`).
- Removed outliers using Z-score.
- Extracted temporal features: `hour`, `month`, `is_weekend`, etc.
- Added rolling and daily average power columns.
- Normalized key features with `MinMaxScaler`.

---

## 🧠 Machine Learning Models

1. Linear Regression
2. Random Forest Regressor
3. Gradient Boosting Regressor
4. MLP Regressor  (Neural Network)

Trained using 80:20 Train-Test Split with random_state = 30

**Best Performer**: Gradient Boosting Regressor

---

## 📊 Visualizations

- Distribution plots of numerical features
- Time Series (Daily & Rolling Averages)
- Correlation Heatmap
- Feature Importance (GBR)
- Actual vs Predicted Scatter Plot

---

## 🔍 Key Insights

- `Sub_metering_3` is the most important predictor of overall household energy usage, followed by `Sub_metering_1` and `Sub_metering_2`.
- Gradient Boosting gave the best generalization performance.
- The correlation analysis showed a very strong linear relationship between Global_active_power and Global_intensity, leading to the removal of the latter to avoid multicollinearity.
- The Actual vs Predicted plot revealed that predictions are generally aligned with true values but tend to underpredict at higher values

---

## 🛠️ Tools & Technologies

- **Python**: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`
- **Notebook**: Jupyter / VS Code
- **Version Control**: Git + GitHub

---

## 🗂️ Folder Structure

Power-Pulse-Household-Energy-Usage-Forecast/
├── household_power_consumption.txt
├── Power_Pulse.ipynb
├──Power Pulse Report.pdf
├── README.md
└── requirements.txt

## Setup Instructions

1. Clone the repository:

        gh repo clone AshvinAK17/Power-Pulse-Household-Energy-Usage-Forecast

2. Install dependencies:

        pip install pandas numpy matplotlib seaborn scikit-learn

3. Run the notebook.
