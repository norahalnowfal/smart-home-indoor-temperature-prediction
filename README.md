# Smart Home Indoor Temperature Prediction

A machine learning project that predicts indoor room temperature using environmental and smart-home sensor data.

The project uses data collected from a solar smart home, including CO₂, relative humidity, lighting, weather, wind, and outdoor humidity measurements.

## Project Objective

The goal is to predict:

`Indoor_temperature_room`

using selected environmental and sensor features.

## Dataset

The training dataset contains:

- 2,764 records
- 19 columns
- No missing values in the original training data

After duplicate removal and IQR-based outlier filtering, 1,629 records remained for modeling.

## Features Used

The Random Forest model was trained using:

- `CO2_room`
- `Relative_humidity_room`
- `Lighting_room`
- `Meteo_Rain`
- `Meteo_Wind`
- `Outdoor_relative_humidity_Sensor`
- `Day_of_the_week`

## Data Preprocessing

The notebook includes:

- Duplicate removal
- Missing-value handling using numeric means
- Date conversion
- IQR-based outlier removal
- Standardization using `StandardScaler`
- Date and time combination into a `DateTime` column
- Exploratory data visualization

## Exploratory Data Analysis

The project visualizes:

- Indoor temperature distribution
- Indoor temperature over time
- Humidity vs. indoor temperature
- CO₂ vs. indoor temperature
- Humidity distribution
- CO₂ distribution
- Humidity over time
- Correlation heatmap

## Machine Learning Model

The prediction model is:

**Random Forest Regressor**

The data was split into:

- 80% training data
- 20% testing data

with `random_state=42`.

## Model Performance

The model achieved:

| Metric | Result |
|---|---:|
| MAE | 0.2013 |
| RMSE | 0.3054 |
| R² Score | **0.9103** |

> Note: The target variable was standardized before model training, so MAE and RMSE are reported in standardized units.

The model explains approximately **91% of the variance** in the test data.

## Feature Importance

The notebook also analyzes feature importance from the trained Random Forest model to show which sensor and environmental variables contribute most to the predictions.

## Project Files

```text
.
├── IOT.ipynb
├── train.csv
├── test.csv
├── sample_submission.csv
├── Solar house sensors and actuators map.png
└── README.md
```

## Smart Home Sensor Map

![Solar House Sensors and Actuators Map](Solar%20house%20sensors%20and%20actuators%20map.png)

## Technologies Used

- Python
- Jupyter Notebook / Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Random Forest Regression

## How to Run

1. Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/smart-home-indoor-temperature-prediction.git
```

2. Open the notebook:

```text
IOT.ipynb
```

3. Install the required libraries if needed:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

4. Run the notebook cells in order.

## Author

**Norah Alnowfal**
