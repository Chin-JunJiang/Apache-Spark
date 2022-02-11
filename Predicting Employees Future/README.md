# Predicting Employees Future

![Projects (2)](https://user-images.githubusercontent.com/91453263/153621139-7b85f558-736b-4118-bf7a-45b6a922cb84.jpeg)

## Project's Objectives
Apache Spark is an open-source, distributed processing system which utilizes in-memory caching, and optimized query execution for fast analytic queries against data of any size.
Apache Spark also has a high performing machine learning library which will be tapped on for this project. The project's objective was to use the machine learning library in 
Apache Spark build a prediction model that can predict the Employees Future in the company with a set of features from the data set.

## Project Description
### Project Flow
The flow of the project is represented by the diagram above. Then raw data set was obtained from the open data source, Kaggle, and uploaded into Amazon S3 storage. 

### Apache Spark 
A cluster was created on Amazon EC2 where Apache Spark 3.1.2 was available. A machine learning pipeline was built with String Indexer, One Hot Encoder and Vector Assembler. 
The categorical columns are passed into the string indexer for the indexing of string values into numerical values and these numerical outputs from the string indexer are 
then passed into the One Hot Encoder. The One Hot Encoder creates a new binary feature for each possible category and assigns a value of 1 to the feature of each sample 
that corresponds to its original category. The categorical columns and the numerical columns are then brought together and passed into the vector assembler which is 
a transformer that combines a given list of columns into a single vector column. The data that passed through the pipeline are then used for training of the folloiwing 
models: Logistic Regression, Decision Tree Regressor, Random Forest Regressor, Gradient Boosted Tree Regressor & Isotonic Regression. The best performing model amongst
the models was the Gradient Boosted Tree Regressor with the lowest Root Mean Square Error of 0.343384.

### Methods Used
* Building Machine Learning Pipeline
* Training and Testing of Machine Learning Models

### Technologies
* Data Bricks (Apache Spark, Spark ML Library)
* AWS (S3 Storage, EC2)
