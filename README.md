# Aircraft-Engine-Remaining-Useful-Life-Prediction-Using-Machine-Learning-Model-
Aircraft Engine RUL Prediction using CMAPSS FD001

This project predicts the Remaining Useful Life (RUL) of aircraft engines using the NASA CMAPSS dataset (FD001 subset). The workflow involves data preprocessing, feature scaling, model training with machine learning (Random Forest), model evaluation, and deployment for predicting RUL of new input data.



 ## Dataset

Source: NASA Prognostics Data Repository

Subset: FD001

Each record represents an engine cycle with:

3 operational settings

21 sensor measurements

RUL (Remaining Useful Life) is computed as:

𝑅
𝑈
𝐿
=
max_cycle_per_engine
−
current_cycle
RUL=max_cycle_per_engine−current_cycle
## Workflow

Data Preprocessing

Drop unused sensors (sensor_1, sensor_5, sensor_10)

Compute RUL for each unit

Normalize features using MinMaxScaler

## Model Training

Split into train (80%) and test (20%)

Train Random Forest Regressor (n_estimators=100)

## Model Evaluation

Metrics used:

Mean Absolute Error (MAE)

Mean Squared Error (MSE)

R² Score

Model Saving

Trained model, scaler, and feature list saved in /model folder

Prediction for New Engine

Input operational settings + sensor values as a dictionary

## Preprocess, scale, and predict RUL using saved model

 Results
 Model Performance (on test set)
MAE: 29.64  
MSE: 1717.62  
R² Score: 0.6241  

 ## Sample Prediction for a New Engine
Predicted Remaining Useful Life (RUL): 201.62 cycles

##  How to Run

Clone this repository

git clone https://github.com/your-username/aircraft-rul-prediction.git




  ## Requirements
pandas  
numpy  
scikit-learn  
matplotlib  
seaborn  
pickle  

 ## Future Improvements

Use deep learning models (e.g., LSTM, GRU) to capture time-series degradation trends

Implement cross-validation for more robust model evaluation

Extend analysis to other CMAPSS subsets (FD002, FD003, FD004)
