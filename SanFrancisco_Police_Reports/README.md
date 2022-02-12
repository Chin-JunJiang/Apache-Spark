# San Francisco Police Reports

![Projects - Page 2](https://user-images.githubusercontent.com/91453263/153695503-f1d37881-da20-4e22-b0d1-a6bb55cf3b8f.png)

## Project's Objectives
Apache Spark is an open-source, distributed processing system which utilizes in-memory caching, and optimized query execution for fast analytic queries against data of any size. 
The project's objective was to use Apache Spark to clean and transform a large data set, utilizing it's in-memory caching for optimised SQL queries execution and visualising 
the queried results through Tableau. 


## Project Description
### Project Flow
The flow of the project is represented by the diagram above. The San Francisco Police Department Incident Reports raw data was obtained from the open data source, DataSF, and 
uploaded into Amazon S3 storage. 

### Apache Spark
A cluster was created on Amazon EC2 where Apache Spark 3.1.2 was available. The data frame schema was defined which included the Structure Field Titles and Type,
and the raw Data in Amazon S3 Storage was read into the defined data frame schema. The data was cleaned and transformed by checking and dropping of null rows and transforming 
of data column for usable analysis. The data was explored using the Spark Data frame API to get a better understanding of the data set. A temporary view of the data frame is created 
which is then cached into memory for optimised queries execution. Sparks SQL queries were executed and the outputs were written to Amazon S3 storage and formatted as csv files. 
The csv files were then loaded into Tableau for the descriptive visualisation of the aggregated data. The cleaned and transformed data frame was written to Amazon S3 storage and formatted as parquet file.

Tableau Visualisation: https://tinyurl.com/SFPoliceReports
![Screenshot (4)](https://user-images.githubusercontent.com/91453263/153253967-0d181681-6e13-47d6-bbeb-69dc9fe49519.png)

### Methods Used
* Data Cleaning and Transformation with Apache Spark (Data Frame API)
* Optimised query Execution with Apache Spark (Spark SQL)
* Data Visualization 

### Technologies
* Data Bricks (Apache Spark)
* AWS (S3 Storage, EC2)
* Tableau
