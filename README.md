# Solar Irradiance Prediction Project Report

## 1. Introduction

This report details a project focused on predicting solar irradiance components—Direct Horizontal Irradiance (DHI), Direct Normal Irradiance (DNI), and Global Horizontal Irradiance (GHI)—using a dataset containing various meteorological features. The project utilizes Python, Pandas, Scikit-learn, and other relevant libraries for data preprocessing, model training, and evaluation. We employ a Random Forest Regressor to predict the solar irradiance components.

## 2. Objectives

The primary objectives were:

* To load and preprocess the meteorological dataset.
* To train a Random Forest Regressor model to predict Clearsky DHI, DNI, and GHI.
* To evaluate the model's performance using appropriate metrics.
* To apply the trained model to predict solar irradiance components for a test dataset.

## 3. Methodology

The project followed these steps:

1.  **Data Loading and Initial Inspection:**
    * Imported necessary Python libraries: Pandas, NumPy, Matplotlib, Seaborn, and Scikit-learn.
    * Loaded the "train (24).csv" dataset into a Pandas DataFrame.
    * Displayed the first few rows of the DataFrame to understand the data's structure.
    * Checked the data types and descriptive statistics.

2.  **Data Preprocessing:**
    * Removed the "Timestamp" column.
    * Checked for missing values and found none.
    * Separated the features (X) and target variables (y_DHI, y_DNI, y_GHI).
    * Standardized the features using StandardScaler.
    * Split the data into training and testing sets for each target variable.

3.  **Model Training and Evaluation:**
    * Trained a Random Forest Regressor model for each target variable (DHI, DNI, GHI).
    * Predicted the target variables for the test sets.
    * Evaluated the model's performance using Mean Squared Error (MSE) and R-squared (R2) score.

4.  **Test Data Prediction:**
    * Loaded the "test (2).csv" dataset.
    * Applied the trained models to predict Clearsky DHI, DNI, and GHI for the test data.

## 4. Dataset Description

The "train (24).csv" dataset contains the following columns:

* **Timestamp:** Time and date of the recorded data.
* **Temperature:** Air temperature in degrees Celsius.
* **Dew Point:** Temperature at which dew forms in degrees Celsius.
* **Surface Albedo:** Fraction of solar energy reflected by the Earth's surface.
* **Pressure:** Atmospheric pressure in hPa.
* **Wind Direction:** Wind direction in degrees.
* **Wind Speed:** Wind speed in meters per second.
* **Clearsky DHI:** Direct Horizontal Irradiance in watts per square meter.
* **Clearsky DNI:** Direct Normal Irradiance in watts per square meter.
* **Clearsky GHI:** Global Horizontal Irradiance in watts per square meter.
* **Fill Flag:** Data filling or correction flag.
* **Ozone:** Ozone concentration in Dobson units.
* **Cloud Type:** Numerical cloud type code.
* **Solar Zenith Angle:** Angle between zenith and the sun.
* **Precipitable Water:** Depth of water from condensed atmospheric moisture in millimeters.
* **Relative Humidity:** Relative humidity percentage.

The "test (2).csv" dataset has the same columns, except for Clearsky DHI, DNI and GHI, which are the target variables to be predicted.

## 5. Results and Observations

* The Random Forest Regressor model demonstrated high performance in predicting DHI, DNI, and GHI.
* The R2 scores for all three predictions were very high, indicating a strong fit between the model and the data.
* The MSE values were relatively low, confirming the model's accuracy.
* The model has been successfully used to predict the DHI, DNI and GHI values for the test dataset.

## 6. Conclusion

This project successfully trained and evaluated a Random Forest Regressor model for predicting solar irradiance components. The model's performance metrics indicate its effectiveness in accurately predicting DHI, DNI, and GHI. The trained model can be used for forecasting solar irradiance in similar meteorological conditions.

## 7. Future Work

Future work on this project could include:

* Exploring other machine learning models, such as Gradient Boosting Regressor or Neural Networks, to potentially improve prediction accuracy.
* Performing hyperparameter tuning to optimize the Random Forest Regressor model.
* Incorporating additional meteorological features or external data sources to enhance the model's predictive capabilities.
* Evaluating the model's performance on a larger and more diverse dataset.
* Time series analysis of the data.
* Apply deep learning models such as LSTMs.
* Use feature selection or feature engineering to improve the model.
