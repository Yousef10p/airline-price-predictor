# Airline Ticket Price Prediction Using Gradient Boosting Regression

## Project Overview
This project predicts **airline ticket prices** using historical flight data. The model uses **Gradient Boosting Regression** to capture complex relationships between flight features and ticket prices.

## Dataset
Features used for prediction:

- **Flight Details:**
  - Duration
  - Total_Stops
  - Day, Month, Year
  - Arrival_Hour, Arrival_Minute
  - Dep_Hour, Dep_Minute

- **Airlines (One-Hot Encoded):**
  - Airline_Air Asia, Airline_Air India, Airline_GoAir
  - Airline_IndiGo, Airline_Jet Airways, Airline_Jet Airways Business
  - Airline_Multiple carriers, Airline_Multiple carriers Premium economy
  - Airline_SpiceJet, Airline_Trujet, Airline_Vistara, Airline_Vistara Premium economy

- **Source Airports:**
  - Source_Banglore, Source_Chennai, Source_Delhi, Source_Kolkata, Source_Mumbai

- **Destination Airports:**
  - Destination_Banglore, Destination_Cochin, Destination_Delhi
  - Destination_Hyderabad, Destination_Kolkata, Destination_New Delhi

- **Additional Info (One-Hot Encoded):**
  - Additional_Info_1 Long layover, Additional_Info_1 Short layover
  - Additional_Info_2 Long layover, Additional_Info_Business class
  - Additional_Info_Change airports, Additional_Info_In-flight meal not included
  - Additional_Info_No Info, Additional_Info_No check-in baggage included
  - Additional_Info_No info, Additional_Info_Red-eye flight

**Target variable:** `Price` (continuous numeric value)

## Data Preprocessing
- Handle missing values in numerical features.  
- Encode categorical features using **One-Hot Encoding**.  
- Scale numerical features using min-max scalling  
- Split the dataset into training and testing sets.

## Why Gradient Boosting?

- Combines multiple decision trees to form a strong predictor.
- Captures non-linear relationships and interactions between features.
- Handles numerical and encoded categorical features effectively.

## Model Evaluation

**Performance metrics:**

- **R² Score (Train):** 0.76
- **R² Score (Test):** 0.71

**Observation:**

- Small difference between train and test R² indicates low overfitting.
- Model provides a reasonably accurate prediction for airline ticket prices.

## Future Improvements

- Feature engineering to include seasonality, holidays, or airline-specific trends.
- Test other ensemble methods (XGBoost, LightGBM, CatBoost).
- Hyperparameter tuning with cross-validation.
- Explore interaction features to further improve accuracy.

## Usage

1. Prepare the dataset with the specified numerical and categorical features.
2. Apply preprocessing: imputation, encoding, and scaling.
3. Train the Gradient Boosting Regressor.
4. Evaluate model performance using R², MAE, RMSE, or other regression metrics.




