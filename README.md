# energy_anomaly_detection

This is a project to detect anomalies for wind turbine active power. For this task, I use the dataset Wind Turbine Scada from Kaggle. By exploring data and doing data analysis, it is a big surprise for me because there are strong linear relationships between features and the target variable. Therefore, a simple linear regression model can solve the problem.

Can we use deep learning to improve the results? I doubt this, because with non-linear activation functions in deep networks, we do not capture well the linear relationships. With more complex data, neural networks may help. Here is a strategy to use deep networks for anomaly detection: we can use autoencoder model to reconstruct data from the latent space and non well-reconstructed data can be seen as anomalies.

UPDATE: I built a simple autoencoder model with keras for the task. The encoder consists of one layer and the decoder consists of two layers. For activation function, we use ReLU. To avoid overfitting, I add L2 regularization in each layer.

RESULTS: The linear model suggests that if |y_pred - y_true| > 400, then there should be anomaly. The autoencoder model suggests if |y_pred - y_true| > 100, there there should be anomaly. To conclude, we would need an expert in electrical engineering to tell us which threshold is good for anomaly detection.

Comments and suggestions are welcome. Thanks for reading!