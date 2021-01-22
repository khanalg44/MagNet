# Weather Forecasting

Job is to write a function that can take seven days of data and make predictions with no additional context.

Your only job is to replace the function predict_dst in benchmark/predict.py with logic that will take seven days worth of data (see the docstring) and output two predictions: one for the current hour (t0) and one for the next hour. See the extensive description on the code submission page.

## Data Preprocessing
- We picked only a few features for the LSTM model.
- converted the data to hourly resulution taking mean and std.
- Used Standard Scaler to scale the data

### Model Building - LSTM
- Tried several things
    - play with batch_size
    - with or without the dropout (with dropout gave better RMSE)
    - Add batch normalization, it didn't improve the result
    - with or without activation function - tried Relu, sigmoid. Relu didn't improve the results 


## Resources
- [Benchmark submission](https://www.drivendata.co/blog/model-geomagnetic-field-benchmark/)
- [DrivenData Git](https://github.com/drivendataorg/noaa-runtime)
- [DrivenData Website](https://www.drivendata.org/competitions/73/noaa-magnetic-forecasting/?fbclid=IwAR3lxCtsCLppvv9ooV36QJCWkP4_g8UT6MwX-TVllWSPQ97zlzEKQpSceHI)
- https://machinelearningmastery.com/how-to-develop-lstm-models-for-time-series-forecasting/ 
- [blog on multivariate time series forecasting](https://towardsdatascience.com/simple-multivariate-time-series-forecasting-7fa0e05579b2)
- https://github.com/Pythonyatra/MagNet
- [VAR Tutorial](https://www.machinelearningplus.com/time-series/vector-autoregression-examples-python/)
- [Nice tutorials on Time-Series Analysis](https://www.machinelearningplus.com/time-series/)
