# Surface Air Temperature Prediction

## Project Objective
The primary objective of this project is to predict the surface air temperature for the next month based on historical monthly mean temperatures. By using both SARIMA and LSTM models, we aim to leverage both statistical and machine learning approaches for time series forecasting and compare their effectiveness.

## Data Preparation
- **Data Source**: The dataset contains monthly mean surface air temperature readings.
- **Data Processing**: The 'month' column was converted to datetime format and set as the index. The data was then scaled and converted into a supervised learning format to prepare it for model training.

## Baseline Model
- **Baseline Approach**: The mean of the past observed values was used as a simple baseline prediction.
- **Evaluation**: The RMSE of the baseline model was calculated to provide a benchmark for comparison with more complex models.

## SARIMA Model
- **Model Description**: SARIMA (Seasonal AutoRegressive Integrated Moving Average) is a statistical model that accounts for seasonality, trend, and noise in time series data.
- **Model Training**: The SARIMA model was trained on the historical temperature data and used to make forecasts.
- **Evaluation**: The model’s performance was evaluated using RMSE, MAE, and residual diagnostics.

## LSTM Model
- **Model Description**: LSTM (Long Short-Term Memory) is a type of recurrent neural network (RNN) designed to learn from sequential data by maintaining long-term dependencies.
- **Data Preparation**: The data was scaled and reshaped for the LSTM model. A look-back window of 12 months was used.
- **Model Training**: The LSTM model was trained with a series of LSTM layers and dropout layers to prevent overfitting.
- **Evaluation**: The model’s performance was evaluated using RMSE and MAE on the test data.

## Combined Model
- **Combination Strategy**: Predictions from both SARIMA and LSTM models were averaged to form a combined forecast.
- **Evaluation**: The combined model’s performance was compared against the baseline model using RMSE.

## XGBoost Model
- **Model Description**: XGBoost is an ensemble learning method based on gradient boosting, designed for high performance and efficiency.
- **Hyperparameter Tuning**: Grid search was used to find the best hyperparameters.
- **Model Training**: The model was trained on the reshaped data and predictions were made.
- **Evaluation**: The performance of the XGBoost model was compared to the baseline model using RMSE.

## Results
- **Model Comparison**: The performance of SARIMA, LSTM, and XGBoost models was evaluated and compared to the baseline model.
- **Best Model**: The model with the lowest RMSE was identified as the best performing model.

## Conclusion
The project demonstrated the application of various time series forecasting models on surface air temperature data. By comparing the performance of statistical and machine learning approaches, the project provided insights into the effectiveness of different models for this specific forecasting task. The XGBoost model outperformed due its capability of fixing the issues of underffiting problems by implementing boosting and regularization techniques. The XGBoost model is able to generalize well on unseen data compared to LSTM model(only for particular dataset).

## Future Work
- **Model Improvement**: Further tuning of hyperparameters and exploring additional features could potentially improve model performance.
- **Additional Models**: Exploring other time series models like Prophet or advanced deep learning models could be beneficial.
- **Feature Engineering**: Incorporating exogenous variables such as geographical data or other climate indicators could improve the accuracy of the predictions.

This project serves as a comprehensive example of time series forecasting, combining traditional statistical methods with modern machine learning techniques to predict future values based on historical data.
