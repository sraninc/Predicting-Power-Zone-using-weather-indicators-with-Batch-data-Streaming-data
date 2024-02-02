# Predicting Power Zone by measuring the impact of weather conditions using batch data & streaming data
In this project, I worked on a dataset downloaded from UCI machine learning repository and then later modified it for the project purposes. The data is based on relating power consumption from different zones of Tetouan city to various factors such as Time of Day(Month/Hour), Temperature, Humidity, Wind speed, and General Diffuse Flows.

The project is divided into two parts
- The first part deals with batch/static data. I used PySpark for the project. I first downloaded the data and read it as a spark SQL data frame. After that, I summarized the data using various numerical summary methods including correlation, means, standard deviation, etc. Then I created a pipeline for a series of transformations(SQL Transformer, Binarizer, OneHotEncoder, PCA Transformer, VectorAssembler). After that I fitted the Elastic Net model with some regularization parameters, the best parameters were chosen using cross-validation. Finally, I estimated the training RMSE on this data.
- The second part of the project is based on streaming data. The streaming data was randomly sampled from three rows of the dataset iteratively. This streaming data was then be used for model transformation and making predictions as was done for the static data.

