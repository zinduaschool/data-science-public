# Data Engineering Curriculum

This course, focusses on Big Data Engineering concepts with an anchoring on Apache Spark and Cloud.  Below is a breakdown of the course:
## Week 1: Introduction to Data Engineering and Data Processing
| Index | Lesson | Content Breakdown | Project/Quiz |
|---|---|---|---|
| 1.1 | What is Data Engineering | Overview of the data engineering role and responsibilities, Introduction to data types: structured, semi-structured, and unstructured data,	Difference between databases, data lakes, and data warehouses | QUIZ: Determine the difference between supervised and unsupervised learning problems |
| 1.2 | Data Ingestion Basics | Overview of data ingestion (batch vs real-time),Introduction to real-time data ingestion tools: Apache Kafka, Hands-on: Set up Apache Kafka and create basic producer and consumer scripts in Python | CHALLENGE: Run a model and test its results on a cross-validation versus a train-test-split |
| 1.3 | Batch Processing with Python and Pandas | Introduction to batch data processing, Hands-on: Load and process CSV data with Python (using Pandas), Perform basic data cleaning and transformation | QUIZ: Determining Tidy Data and how to outlier and missing data |
| 1.4 | Introduction to NoSQL databases | Overview of NoSQL databases and comparison with SQL databases, Introduction to MongoDB and its use cases, Hands-on: Set up MongoDB locally, insert, and query data | CHALLENGE: Given a dataset, conduct data preprocessing to output clean data for machine learning |
| 1.5 | Project | Project: Build a data ingestion pipeline using Apache Kafka that ingests streaming data (e.g., stock prices or weather data) and stores it in MongoDB. Include basic data transformation using Python | | |

## Week 2: Data Processing with Apache Spark

| Index | Lesson | Content Breakdown | Project/Quiz |
|-------|--------|-------------------|--------------|
| 2.1 | Introduction to Apache Spark | • Overview of Apache Spark and its architecture<br>• Difference between batch and real-time processing in Spark | - |
| 2.2 | DataFrames and Spark SQL | • Introduction to Spark DataFrames<br>• Hands-on: Load CSV data into Spark and perform basic transformations<br>• Introduction to Spark SQL for querying large datasets | - |
| 2.3 | Data Aggregation and Transformation in Spark | • Learn about groupBy, filter, and other Spark transformations<br>• Hands-on: Perform aggregations and join operations on datasets | - |
| 2.4 | Introduction to Spark Streaming | • Overview of Spark Streaming for real-time data processing<br>• Hands-on: Set up a simple Spark Streaming application to process real-time data (e.g., using data from Apache Kafka) | - |
| 2.5 |  Project 2 | - | Create an Apache Spark application to process a large batch dataset, perform transformations, and load the processed data into a NoSQL database like MongoDB. Include real-time data streaming with Spark Streaming. |

## Week 3: ETL and Data Warehousing

| Index | Lesson | Content Breakdown | Project/Quiz |
|-------|--------|-------------------|--------------|
| 3.1 | What is ETL (Extract, Transform, Load)? | • Introduction to ETL pipelines and their importance in data engineering<br>• Hands-on: Write a basic ETL script in Python to extract data from a CSV file, transform it, and load it into a SQL database | - |
| 3.2 | Introduction to SQL and Relational Databases | • Basic SQL commands: SELECT, INSERT, UPDATE, DELETE<br>• Hands-on: Set up a relational database (e.g., PostgreSQL) and practice querying with SQL | - |
| 3.3 | Data Warehousing Basics | • Overview of data warehouses (e.g., AWS Redshift, Snowflake)<br>• Differences between data warehouses and databases<br>• Introduction to star and snowflake schemas | - |
| 3.4 | Automating ETL Workflows | • Introduction to Apache Airflow for automating and orchestrating ETL workflows<br>• Hands-on: Set up Airflow locally and create a simple DAG (Directed Acyclic Graph) to schedule an ETL pipeline | - |
| 3.5 |  Project 3 | - | Build a simple ETL pipeline using Python and Airflow. Extract data from a CSV file, transform it using Spark, and load it into a relational database like PostgreSQL or an online data warehouse service (e.g., AWS Redshift). |

## Week 4: Data Orchestration, Cloud Platforms, and Data Governance

| Index | Lesson | Content Breakdown | Project/Quiz |
|-------|--------|-------------------|--------------|
| 4.1 | Introduction to Data Pipeline Orchestration | • Overview of orchestration tools (Apache Airflow, Prefect)<br>• Hands-on: Build an automated ETL pipeline using Apache Airflow | - |
| 4.2 | Introduction to Cloud Platforms for Data Engineering | • Overview of cloud platforms: AWS, Google Cloud, Azure<br>• Introduction to cloud-based storage solutions (AWS S3, Google Cloud Storage)<br>• Hands-on: Upload data to a cloud storage service (e.g., AWS S3) and manage the data | - |
| 4.3 | Data Governance and Quality | • Understanding data governance and why it's important in data engineering<br>• Introduction to data validation and monitoring tools<br>• Hands-on: Validate data for quality using Python (e.g., Pandas or Great Expectations) | - |
| 4.4 | Introduction to Cloud Data Warehousing | • Overview of cloud data warehouses (Google BigQuery, AWS Redshift)<br>• Hands-on: Query a large dataset using a cloud data warehouse service | - |
| 4.5 |  Project 4 | - | Use Apache Airflow to orchestrate a cloud-based ETL pipeline. Extract data from cloud storage (e.g., AWS S3), process it using Spark, and load it into a cloud data warehouse like AWS Redshift or Google BigQuery. |

## Week 5: Performance Optimization and Scalability

| Index | Lesson | Content Breakdown | Project/Quiz |
|-------|--------|-------------------|--------------|
| 5.1 | Introduction to Performance Optimization | • Overview of performance bottlenecks in data pipelines<br>• Importance of optimizing data transformations and queries<br>• Hands-on: Identify performance issues in a sample data pipeline | - |
| 5.2 | Query Optimization in SQL and Spark | • Learn how to use query execution plans in SQL databases and Apache Spark<br>• Techniques like indexing, partitioning, and caching<br>• Hands-on: Optimize queries in PostgreSQL and Spark Data Frames | - |
| 5.3 | Scaling Data Pipelines | • Overview of vertical and horizontal scaling<br>• Best practices for scaling data workflows in distributed systems<br>• Hands-on: Scale a Spark application to handle larger datasets | - |
| 5.4 | Distributed Storage and Processing | • Introduction to distributed file systems (HDFS, S3) and their role in scalability<br>• Data partitioning strategies for distributed systems<br>• Hands-on: Use partitioning and bucketing in Apache Hive or Spark | - |
| 5.5 | Project 5 | - | Optimize an existing ETL pipeline for performance and scalability. Analyze the pipeline for bottlenecks. Implement improvements (e.g., optimized SQL queries, caching, partitioning). Test the pipeline's performance before and after optimization. |

## Week 6: Advanced Topics in Data Engineering

| Index | Lesson | Content Breakdown | Project/Quiz |
|-------|--------|-------------------|--------------|
| 6.1 | Introduction to Data Lakehouse and Delta Lake | • Differences between data lakes, warehouses, and lakehouses<br>• Use cases for Delta Lake in modern data engineering<br>• Hands-on: Set up a Delta Lake and perform simple data operations | - |
| 6.2 | Streaming Data Processing with Advanced Tools | • Introduction to advanced streaming platforms (Flink, Kafka Streams)<br>• Event-time processing and handling late-arriving data<br>• Hands-on: Build a real-time data stream processing pipeline using Flink | - |
| 6.3 | Data Mesh Architecture | • Overview of the data mesh concept and principles<br>• Decentralized data ownership and domain-oriented data products<br>• Hands-on: Design a simple data mesh architecture for a hypothetical organization | - |
| 6.4 | Machine Learning for Data Engineers | • Preparing data for machine learning pipelines<br>• Using tools like TensorFlow Data Validation (TFDV) for quality checks<br>• Hands-on: Build a simple feature engineering pipeline for ML | - |
| 6.5 |  Project 6 | - | Build a Delta Lake-based data pipeline that ingests streaming data and supports both batch and real-time analytics. Include monitoring and alerting for data quality. |

## Week 7: Real-Time Analytics and Monitoring

| Index | Lesson | Content Breakdown | Project/Quiz |
|-------|--------|-------------------|--------------|
| 7.1 | Real-Time Analytics Fundamentals | • Key differences between batch and real-time analytics<br>• Tools for real-time analytics (e.g., Elasticsearch, Druid, Apache Pinot)<br>• Hands-on: Query real-time data using Apache Druid | - |
| 7.2 | Monitoring Data Pipelines | • Introduction to monitoring tools (Prometheus, Grafana)<br>• Setting up alerts for pipeline failures or data anomalies<br>• Hands-on: Monitor a sample data pipeline with Grafana and Prometheus | - |
| 7.3 | Real-Time Dashboards | • Building dashboards for real-time data visualization (e.g., Tableau, Power BI, or Superset)<br>• Best practices for dashboard design<br>• Hands-on: Create a real-time dashboard using Superset or Tableau | - |
| 7.4 | Advanced Real-Time Use Cases | • Applications like fraud detection, IoT analytics, and user behavior tracking<br>• Hands-on: Implement real-time analytics use case (e.g., anomaly detection for streaming data) | - |
| 7.5 | Project 7 | - | Build an end-to-end real-time analytics pipeline. Ingest streaming data using Kafka. Process and analyze data in real time using Spark Streaming. Visualize insights on a real-time dashboard with Grafana or Tableau. |

## Week 8 - 10: Real-World Project

| Index | Lesson | Content Breakdown | Project/Quiz |
|-------|--------|-------------------|--------------|
| 8.1 | Real-World Project Implementation | End-to-end data pipeline implementation focusing on retail sales data processing pipeline | Implement a Real-World Data Engineering Project:<br>• **Step 1:** Ingest sales data (CSV or streaming via Kafka) into a cloud storage solution (AWS S3 or Google Cloud Storage)<br>• **Step 2:** Process the data using Apache Spark (data cleaning, transformations)<br>• **Step 3:** Load processed data into a cloud data warehouse (AWS Redshift or Google Big Query)<br>• **Step 4:** Automate the pipeline with Apache Airflow, ensuring data quality checks are in place |
