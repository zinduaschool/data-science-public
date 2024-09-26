# Data Engineering Curriculum

This course, focusses on Big Data Engineering concepts with an anchoring on Apache Spark.  Below is a breakdown of the course:
## Week 1: Introduction to Data Engineering and Data Processing
| Index | Lesson | Content Breakdown | Project/Quiz |
|---|---|---|---|
| 1.1 | What is Data Engineering | Overview of the data engineering role and responsibilities, Introduction to data types: structured, semi-structured, and unstructured data,	Difference between databases, data lakes, and data warehouses | QUIZ: Determine the difference between supervised and unsupervised learning problems |
| 1.2 | Data Ingestion Basics | Overview of data ingestion (batch vs real-time),Introduction to real-time data ingestion tools: Apache Kafka, Hands-on: Set up Apache Kafka and create basic producer and consumer scripts in Python | CHALLENGE: Run a model and test its results on a cross-validation versus a train-test-split |
| 1.3 |Batch Processing with Python and Pandas | Introduction to batch data processing, Hands-on: Load and process CSV data with Python (using Pandas), Perform basic data cleaning and transformation | QUIZ: Determining Tidy Data and how to outlier and missing data |

| 1.4 | Introduction to NoSQL databases | Overview of NoSQL databases and comparison with SQL databases, Introduction to MongoDB and its use cases, Hands-on: Set up MongoDB locally, insert, and query data | CHALLENGE: Given a dataset, conduct data preprocessing to output clean data for machine learning |

| 1.5 | Project | Project: Build a data ingestion pipeline using Apache Kafka that ingests streaming data (e.g., stock prices or weather data) and stores it in MongoDB. Include basic data transformation using Python | | |

## Week 2: Regression
| Index | Lesson | Content Breakdown | Project/Quiz |
|---|---|---|---|
| 2.1 | Linear Regression | Model Intution, Gradient Descent, Scikit Learn Example |  |
| 2.2 | Advanced Linear Regression | Multivariable Regression, Feature Scaling, Polynomial Features |  |
| 2.3 | Logisitic Regression | Model Intitution, Gradient Descent, Scikit Learn Example |  |
| 2.4 | Regularisation | The Overfitting Problem, L1 vs L2 Regularisation, Scikit Learn Example |  |
| 2.5 | Regression Project | PROJECT involving the prediction of a continuous variable (Car Price or House Price) |  |

## Week 3: Classification
| Index | Lesson | Content Breakdown | Project/Quiz |
|---|---|---|---|
| 3.1 | K-Nearest & Naives Bayes |  |  |
| 3.2 | Support Vector Machines |  |  |
| 3.3 | Trees & Ensemble Methods |  |  |
| 3.4 | Handling Class Imbalances |  |  |
| 3.5 | Classification Project |  |  |

## Week 4: Model Evaluation & Deployment
| Index | Lesson | Content Breakdown | Project/Quiz |
|---|---|---|---|
| 4.1 | Model Evaluation | Regression Metrics, Classification Metrics, Confusion Matrix |  |
| 4.2 | Hyperparameter Tuning | Grid Search CV, Working with Pipelines, Learning Curves |  |
| 4.3 | Error Analysis |  |  |
| 4.4 | Streamlit Deployment |  |  |
| 4.5 | End-to-end ML Project |  |  |

## Week 5: Machine Learning Capstone
Student can choose to work on one of the following projects:
1. Regression Capstone
2. Classification Capstone 
3. Image Classification Capstone

## Next Steps – Machine Learning II
The following machine learning topics will be covered in the advanced machine learning course:
1. **Unsupervised Learning:** Clustering, Anomaly Detection, Dimensionality Reduction
2. **Time Series Analysis:** ARIMA Model, ANOVA Model, ARCH/GARCH Model
3. **Neural Networks:** Perceptron, CNN (Computer Vision), RNN (Sequential Data), NLP

________________________________________
Week 2: Data Processing with Apache Spark
Day 1-4: Learning Concepts
●	Day 1: Introduction to Apache Spark
○	Overview of Apache Spark and its architecture
○	Difference between batch and real-time processing in Spark
●	Day 2: DataFrames and Spark SQL
○	Introduction to Spark DataFrames
○	Hands-on: Load CSV data into Spark and perform basic transformations
○	Introduction to Spark SQL for querying large datasets
●	Day 3: Data Aggregation and Transformation in Spark
○	Learn about groupBy, filter, and other Spark transformations
○	Hands-on: Perform aggregations and join operations on datasets
●	Day 4: Introduction to Spark Streaming
○	Overview of Spark Streaming for real-time data processing
○	Hands-on: Set up a simple Spark Streaming application to process real-time data (e.g., using data from Apache Kafka)
Day 5: Capstone Project 2
●	Project: Create an Apache Spark application to process a large batch dataset, perform transformations, and load the processed data into a NoSQL database like MongoDB. Include real-time data streaming with Spark Streaming.
________________________________________
Week 3: ETL and Data Warehousing
Day 1-4: Learning Concepts
●	Day 1: What is ETL (Extract, Transform, Load)?
○	Introduction to ETL pipelines and their importance in data engineering
○	Hands-on: Write a basic ETL script in Python to extract data from a CSV file, transform it, and load it into a SQL database
●	Day 2: Introduction to SQL and Relational Databases
○	Basic SQL commands: SELECT, INSERT, UPDATE, DELETE
○	Hands-on: Set up a relational database (e.g., PostgreSQL) and practice querying with SQL
●	Day 3: Data Warehousing Basics
○	Overview of data warehouses (e.g., AWS Redshift, Snowflake)
○	Differences between data warehouses and databases
○	Introduction to star and snowflake schemas
●	Day 4: Automating ETL Workflows
○	Introduction to Apache Airflow for automating and orchestrating ETL workflows
○	Hands-on: Set up Airflow locally and create a simple DAG (Directed Acyclic Graph) to schedule an ETL pipeline
Day 5: Capstone Project 3
●	Project: Build a simple ETL pipeline using Python and Airflow. Extract data from a CSV file, transform it using Spark, and load it into a relational database like PostgreSQL or an online data warehouse service (e.g., AWS Redshift).
________________________________________
Week 4: Data Orchestration, Cloud Platforms, and Data Governance
Day 1-4: Learning Concepts
●	Day 1: Introduction to Data Pipeline Orchestration
○	Overview of orchestration tools (Apache Airflow, Prefect)
○	Hands-on: Build an automated ETL pipeline using Apache Airflow
●	Day 2: Introduction to Cloud Platforms for Data Engineering
○	Overview of cloud platforms: AWS, Google Cloud, Azure
○	Introduction to cloud-based storage solutions (AWS S3, Google Cloud Storage)
○	Hands-on: Upload data to a cloud storage service (e.g., AWS S3) and manage the data
●	Day 3: Data Governance and Quality
○	Understanding data governance and why it’s important in data engineering
○	Introduction to data validation and monitoring tools
○	Hands-on: Validate data for quality using Python (e.g., Pandas or Great Expectations)
●	Day 4: Introduction to Cloud Data Warehousing
○	Overview of cloud data warehouses (Google BigQuery, AWS Redshift)
○	Hands-on: Query a large dataset using a cloud data warehouse service
Day 5: Capstone Project 4
●	Project: Use Apache Airflow to orchestrate a cloud-based ETL pipeline. Extract data from cloud storage (e.g., AWS S3), process it using Spark, and load it into a cloud data warehouse like AWS Redshift or Google BigQuery.
________________________________________
Week 5: Real-World Project
Project Week: Implement a Real-World Data Engineering Project
●	Project Focus: End-to-end data pipeline implementation.
○	Example: Building a retail sales data processing pipeline
■	Step 1: Ingest sales data (CSV or streaming via Kafka) into a cloud storage solution (AWS S3 or Google Cloud Storage)
■	Step 2: Process the data using Apache Spark (data cleaning, transformations)
■	Step 3: Load processed data into a cloud data warehouse (AWS Redshift or Google BigQuery)
■	Step 4: Automate the pipeline with Apache Airflow, ensuring data quality checks are in place
Deliverables:
●	A fully functional data pipeline
●	Documentation explaining the design, tools used, and challenges faced
