# 🌡️ Temperature Forecast Project Using ML

## 📌 Project Overview

This project uses Machine Learning to forecast the **next day's maximum and minimum temperature** based on historical weather observations and atmospheric conditions.

The dataset contains weather information such as present maximum and minimum temperature, humidity, wind speed, cloud cover, precipitation, geographical information, DEM, slope, and solar radiation. The prediction targets are `Next_Tmax` and `Next_Tmin`.

## 🎯 Objectives

* Predict the next day's maximum temperature.
* Predict the next day's minimum temperature.
* Analyze weather-related features.
* Handle missing values in the dataset.
* Train a regression model for temperature forecasting.
* Evaluate model performance using regression metrics.

## 📊 Dataset

The dataset contains **7,752 records and 25 columns**. Most columns are numerical, while `Date` is stored as an object column.

### Important Features

* `station`
* `Present_Tmax`
* `Present_Tmin`
* `LDAPS_RHmin`
* `LDAPS_RHmax`
* `LDAPS_Tmax_lapse`
* `LDAPS_Tmin_lapse`
* `LDAPS_WS`
* `LDAPS_LH`
* `LDAPS_CC1` to `LDAPS_CC4`
* `LDAPS_PPT1` to `LDAPS_PPT4`
* `lat`
* `lon`
* `DEM`
* `Slope`
* `Solar radiation`

### Target Variables

* `Next_Tmax` – Next day's maximum temperature
* `Next_Tmin` – Next day's minimum temperature

## 🔧 Data Preprocessing

The project performs the following preprocessing steps:

1. Loads the dataset using Pandas.
2. Checks the dataset structure and data types.
3. Checks missing values.
4. Removes the `Date` column for model preparation.
5. Fills missing numerical values using the median.
6. Verifies that missing values have been handled.

## 🤖 Machine Learning Model

The project uses **XGBoost Regressor** for temperature prediction.

The model is configured with:

* `n_estimators = 300`
* `learning_rate = 0.05`
* `max_depth = 6`
* `subsample = 0.8`
* `colsample_bytree = 0.8`

The model is trained using the training dataset and used to predict temperature values on the test dataset.

## 📈 Model Evaluation

The model performance is evaluated using:

* **MAE (Mean Absolute Error)**
* **MSE (Mean Squared Error)**
* **RMSE (Root Mean Squared Error)**
* **R² Score**

These metrics are calculated using the actual and predicted temperature values.

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost
* KaggleHub
* Jupyter Notebook / Google Colab

## 📁 Project Structure

```text
Temperature-Forecast-Project/
│
├── Temperature_Forecast_Project_using_ML.ipynb
├── README.md
└── temp.csv
```

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone <your-repository-link>
```

### 2. Install required libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost kagglehub
```

### 3. Open the notebook

Open:

```text
Temperature_Forecast_Project_using_ML.ipynb
```

### 4. Run all cells

Execute the notebook cells sequentially to load the dataset, preprocess the data, train the XGBoost model, generate predictions, and evaluate performance.

## 🔮 Future Improvements

* Add advanced feature engineering using date information.
* Compare XGBoost with Random Forest and other regression algorithms.
* Perform hyperparameter tuning.
* Build a Streamlit web application for interactive temperature prediction.
* Save the trained model for future predictions.

## 👨‍💻 Author

**Hemant Rajput**

---

⭐ If you find this project useful, consider giving the repository a star!
