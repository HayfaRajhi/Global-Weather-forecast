# Global Weather Forecasting and Climate Analysis
## PM Accelerator mission
Welcome to PM Accelerator, a beacon of guidance for aspiring and experienced PMs alike. We’ve designed this platform to offer training, education, and job opportunities for Product Managers, creating room for constant improvement and shaping the next generation of PMs. Whether you’re a newbie or you’ve spent years in the industry, you’re guaranteed to find a new opportunity with the help of PM Accelerator.  

By making industry-leading tools and education available to individuals from all backgrounds, we level the playing field for future PM leaders. This is the PM Accelerator motto, as we grant aspiring and experienced PMs what they need most – Access. We introduce you to industry leaders, surround you with the right PM ecosystem, and discover the new world of AI product management skills.


## Project Overview 

This project aims to develop a robust time series forecasting model for predicting weather parameters across multiple countries. The dataset includes various features such as temperature, precipitation, wind speed, and air quality, collected over time for different countries. The project incorporates *machine learning* ,*time series* and *deep learning* techniques to predict weather conditions while analyzing climate trends and geographical patterns.  

## Objectives

- Time Series Forecasting: Build a predictive model for weather parameters, focusing on temperature as the primary target.

- Climate Analysis: Analyze long-term climate trends and variations in different regions.

- Environmental Impact: Study air quality correlations with other weather parameters.

- Feature Importance: Evaluate the importance of each feature using advanced techniques.

## Methodology

**1. Data Preparation**

*Dataset:* The dataset contains weather data collected from multiple countries, with fields such as date, country, temperature, precipitation, wind speed, and air quality.

*Encoding:* The Country column was one-hot encoded to make it machine-readable.

*Normalization:* Continuous features were scaled using MinMaxScaler to bring them to a similar range.

*Lag Features:* Lagged features were created to incorporate temporal dependencies for better forecasting.

**2. Exploratory Data Analysis (EDA)**

Plotted historical weather trends for each country.

Visualized geographical differences in temperature and precipitation.

Analyzed feature correlations to identify key drivers of weather conditions.

**3. Model Building**

### a. ARIMA (Auto-Regressive Integrated Moving Average):

Implemented for univariate time series forecasting of temperature and precipitation.

Steps:

Conducted stationarity tests using ADF (Augmented Dickey-Fuller) test.

Differenced the data to achieve stationarity.

Optimized ARIMA parameters (p, d, q) using AIC and BIC scores.

Limitations: Performed well for individual countries but struggled with multivariate datasets.


### b. LSTM (Long Short-Term Memory):

A recurrent neural network model was implemented to capture sequential dependencies in the data.

Architecture:

Input layer with lagged features.

LSTM layers with 64 units.

Dense layers for final predictions.

Training: The model was trained on time-indexed data with an 80-20 train-validation split.

### c. Random Forest Regressor:

Used as a baseline model for comparison.

Handles tabular data efficiently and provides feature importance metrics.

**4. Evaluation**

The models were evaluated using the following metrics:

- Mean Absolute Error (MAE)

- Root Mean Squared Error (RMSE)

Performance was analyzed per country to evaluate the model's adaptability across regions.

**5. Visualization**

Plotted actual vs. predicted temperature values for each country.

Mapped geographical patterns using libraries like Matplotlib and Seaborn.

## Results

### Model Performance

**ARIMA:** Delivered reliable forecasts for stationary univariate time series but lacked adaptability for multivariate data.

**LSTM:** Achieved lower MAE and RMSE compared to the Random Forest model, especially for countries with larger datasets.

**Random Forest:** Performed well for countries with less temporal variation but struggled with sequential dependencies.



## Tools and Technologies

*Languages: Python*

*Libraries: Pandas, NumPy, TensorFlow, Scikit-learn, Matplotlib, Seaborn*

*Frameworks: Jupyter Notebook for development*

## How to Run the Project

Clone the repository:

    git clone ttps://github.com/HayfaRajhi/Global-Weather-forecast.git

    cd global-weather-forecast

Install dependencies:

    pip install -r requirements.txt

Prepare the data:

Place the weather dataset in the data/raw_data directory.

Run the Jupyter Notebook:

    jupyter notebook global_weather_forecast.ipynb

Evaluate the models and visualize results.
