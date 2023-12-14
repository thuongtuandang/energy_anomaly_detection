# energy_anomaly_detection

This is a project to detect anomalies for wind turbine active power. For this task, I use the dataset Wind Turbine Scada from Kaggle. It is a big surprise for me because there are strong linear relationships between features and the target variable. Therefore, a simple linear regression model can solve the problem.

Can we use deep learning to improve the results? I doubt this, because with non-linear activation functions in deep networks, we do not capture well the linear relationships. With more complex data, neural networks may help. Here is a strategy to use deep networks for anomaly detection: we can use autoencoder model to reconstruct data from the latent space and non well-reconstructed data can be seen as anomalies.

UPDATE: I built a simple autoencoder model for the task. The model has two layers: encoder layer and decoder layer, and both use ReLU activation function. There is a problem: the model is not stable, it is very sensitive to hyperparameters, for example, learning rate or hidden size. However, in case it runs well, the result is similar to the linear model.

Comments and suggestions are welcome. Thanks for reading!