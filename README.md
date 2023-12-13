# energy_anomaly_detection

This is a project to detect anomalies for wind turbin active power. For this task, I use the dataset Wind Turbine Scada from Kaggle. It is a big surprise for me because there are strong linear relationships between features and the target variable. Therefore, a simple linear regression model can solve the problem.

Can we use deep learning to improve the results? I doubt this, because with non-linear activation functions in deep networks, we do not capture well the linear relationships. With more complex data, neural networks may help. Here is a strategy to use deep networks for anomaly detection:

- Problem restatement: We can restate the problem, for example, use data of three previous days to predict the active power of the next day.
- For model, we can use autoencoders to construct data from latent space. Non well-reconstructed data can be seen as anomalies.