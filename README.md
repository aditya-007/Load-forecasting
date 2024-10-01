# Load-forecasting
Load forecasting with machine learning.
## Load data
Load data have been taken from Electrical Reliability Council of Texas (ERCOT). The dataset consists of the following columns:
    Date: Timestamp of the reading.
    DryBulb: Dry bulb temperature (°C).
    DewPnt: Dew point temperature (°C).
    WetBulb: Wet bulb temperature (°C).
    Humidity: Humidity (%).
    ElecPrice: Electricity price ($/MWh).
    Day: Day of the month.
    Month: Month of the year.
    Year: Year of the data.
    Minutes: Time in minutes (since midnight).
    SYSLoad: The system load (the target variable for prediction).

The other dataset from Schneider Electric used in this project is a time-series dataset stored in train.csv. It consists of 46 features, including:

    Temperature measurements from various tanks and environmental locations.
    Radiation, humidity, and occupancy levels.
    
## ML Model
LSTM model has been used in this project. LSTM models such as the ones we’ll be using here are critical to load forecasting. 
The following three models have been used with the details as follows:
- LSTM1 (Simple Model): A single LSTM layer with 50 units.
- LSTM2 (Complex Model): Two LSTM layers with 100 and 50 units.
- LSTM3 (Complex Model 2): Two LSTM layers with 128 and 64 units, dropout regularization, and a dense layer with ReLU activation.

Incorporating excessive layers and hidden nodes can lead to overfitting, resulting in a model that excels on training data but struggles in real-world applications. Conversely, a model that is too simplistic may yield subpar predictions for both training and test data.


## Results
To test the model's accuracy, the mean absolute percentage error (MAPE) and root mean square error (RMSE) will be used. Following graphs show the predicted vs actual trend on the test set.

![LSTM3_test_result](https://github.com/user-attachments/assets/ebe11f78-ff71-4096-8da4-123c244668d0)
