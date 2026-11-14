# Specialization: Big Data Engineering
Official Curriculum for the Big Data Engineering Course in the Data Roadmap.

- **Course Description:** A 12-week course that takes engineers from the data engineering lifecycle to a production-grade data platform. Learners build progressively — reproducible infrastructure, then batch and streaming ingestion, then orchestrated pipelines, then storage architecture and distributed processing in Spark — before extending the platform to machine learning and AI workloads. Theoretical content is cloud-agnostic, while practical labs and projects are anchored on **AWS** for a consistent hands-on experience. Data governance and security are woven throughout the course rather than taught as a standalone topic.

- **Course Objective:** Equip learners to design, build, orchestrate, secure and operate data platforms that move data reliably at scale, and to justify their architectural decisions on latency, correctness, cost and governance grounds rather than tool preference.

- **Skills to be learned:** Docker & Docker Compose, Terraform, GitHub Actions, REST APIs & Postman, web scraping (requests/BeautifulSoup), Change Data Capture & Debezium, Apache Kafka, Amazon Kinesis, Apache Airflow 3, PostgreSQL, MongoDB, dbt Core, Parquet & Avro, S3 data lakes, Delta Lake & the medallion architecture, Apache Spark (PySpark, Spark SQL, Structured Streaming), Spark MLlib, MLflow, feature stores (Feast), Metabase, AWS (S3, EC2, IAM), prompt engineering & MCP

## Curriculum Breakdown

**Module 1: Foundations and Engineering Practice (Weeks 1–2)**
> **Module Objective:** Establish the vocabulary of the field and the engineering discipline it is practised with, at the same time. Learners leave able to reason about lifecycle, architecture, storage formats and governance in the abstract, and to stand up the reproducible, containerised, version-controlled AWS infrastructure that the rest of the course runs on.

### Week 1: Data Engineering Fundamentals
> **Objective:** Establish the mental model and design constraints of the field: learners will be able to describe the data engineering lifecycle and place any role, tool or layer inside it, distinguish batch from streaming and ETL from ELT against a stated requirement, choose a file format and compression scheme and defend it on splittability and query cost, and treat idempotency, data contracts, quality dimensions, lineage and PII handling as constraints on a design rather than as afterthoughts.

| Index | Lesson | Content Breakdown | Project/Quiz |
|---|---|---|---|
| 1.1 | Core Concepts | Introduction to Data Engineering, Roles, and Responsibilities | - |
| 1.2 | Big Data Architecture | Architecture components and layers; Lambda vs Kappa; data lakes, warehouses, marts, and swamps; the Modern Data Stack | QUIZ 1: Days 1–2 Fundamentals |
| 1.3 | ETL vs ELT & Pipeline Principles | Batch vs Streaming, Idempotency, Data Contracts, and Pipeline Design | - |
| 1.4 | Scalable Storage and Access | File Formats (Parquet, Avro), Compression, and Distributed Storage | - |
| 1.5 | Data Governance Primer | Data Quality, Lineage, Security, and Compliance (GDPR/PII) — revisited across the course | QUIZ 2: Days 3–5 Pipelines, Storage & Governance |
| 1.6 | **Optional:** Cloud Fundamentals | Introduction to Cloud Computing; Creating an AWS Account (root vs IAM, console vs CLI, access keys, MFA); AWS Global Infrastructure & Regions; Cost Management, Free Tier & Billing Alerts — for learners new to cloud/AWS before Week 2 | VIDEO: AWS Account Setup Walkthrough |

> **Note on 1.6:** This optional day is recommended if you are not yet comfortable with cloud computing or AWS. The rest of the course uses AWS for hands-on labs from Week 2 onward. There is no project for this day—follow the lesson markdowns and companion video instead.

### Week 2: DevOps for Data Engineering
> **Objective:** Treat data infrastructure as code rather than as clicks: learners will be able to containerise a Python data workload and run a multi-service stack with Docker Compose, provision AWS infrastructure declaratively with Terraform and tear it down cleanly, explain environment isolation and promotion across Dev, UAT and Prod, and express a build-and-deploy workflow in GitHub Actions.

| Index | Lesson | Content Breakdown | Project/Quiz |
|---|---|---|---|
| 2.1 | Introduction to Docker | Containers vs VMs, Images, Dockerfile basics, and Docker Compose essentials | - |
| 2.2 | Multi-Container Data Stacks | Orchestrating services (e.g., Postgres + PgAdmin + Python ETL) with Compose | QUIZ 1: Days 1–2 Docker & Stacks |
| 2.3 | Infrastructure as Code | Terraform basics: providers, resources, state, and spinning up an EC2/S3 resource on AWS | - |
| 2.4 | CI/CD for Data Pipelines | GitHub Actions, Dev/UAT/Prod environments, and promotion strategies | QUIZ 2: Days 3–4 IaC & CI/CD |
| 2.5 | Project 1 | **Phased build:** Terraform (S3 + IAM + EC2) → land sample CSV → Dockerized Python on EC2 reads S3 and plots one metric (pandas/matplotlib) → optional GitHub Actions for IaC + workload | DevOps Project |

**Module 2: Data Ingestion and Orchestration (Weeks 3–6)**
> **Module Objective:** Get data into the platform and keep it arriving reliably. Learners leave able to ingest from REST APIs, web pages, operational databases and event streams, and to schedule, orchestrate, monitor and recover those pipelines in Airflow rather than running them by hand.

### Week 3: Data Ingestion — Batch
> **Objective:** Get data out of systems that were not designed to hand it over: learners will be able to extract from an authenticated, paginated REST API with rate-limit-aware retries, read API documentation well enough to plan a pipeline before writing it, scrape a static page legally and defensively when no API exists, and choose between full loads, watermarked incrementals, CDC and managed connectors for a database source.

| Index | Lesson | Content Breakdown | Project/Quiz |
|---|---|---|---|
| 3.1 | REST APIs | HTTP Methods, JSON, Status Codes, and API design principles | - |
| 3.2 | Working with APIs | Hands-on with Postman, Extracting data from external APIs (e.g., Weather/Finance) | QUIZ 1: Days 1–2 REST APIs & Working with APIs |
| 3.3 | Web Scraping | Extracting data from HTML, handling pagination and rate limiting | - |
| 3.4 | Ingesting from Databases | JDBC, batch ingestion patterns, and incremental loads | QUIZ 2: Days 3–4 Web Scraping & Database Ingestion |
| 3.5 | Project 2 | **Guided build:** CoinGecko API ingestion (auth + pagination) → Parquet + metadata in S3 on Project 1 infrastructure; Terraform public-read URL for submission | Batch Ingestion Project |

### Week 4: Data Ingestion — Streaming
> **Objective:** Move from pulling data to receiving it: learners will be able to explain event-driven architecture in terms of producers, consumers, topics, partitions, keys and offsets, stand up a Kafka cluster and reason about brokers, replication and delivery semantics, weigh self-managed Kafka against managed Kinesis, and recognise IoT telemetry, clickstreams and CDC as the event sources that justify streaming.

| Index | Lesson | Content Breakdown | Project/Quiz |
|---|---|---|---|
| 4.1 | Streaming Fundamentals | Event-Driven Architecture, Producers & Consumers, Topics & Partitions, and Kafka in Action (Docker Setup) | - |
| 4.2 | Apache Kafka | Kafka architecture, Brokers & Clusters, and Managing Consumer Offsets | QUIZ 1: Days 1–2 Streaming Fundamentals & Kafka |
| 4.3 | Cloud Streaming on AWS | Kinesis Data Streams & Firehose as managed alternatives to Kafka | - |
| 4.4 | Real-World Streaming Use Cases | Real-World Event Sources (IoT & Clickstreams) and CDC with Debezium | QUIZ 2: Days 3–4 Cloud Streaming & Real-World Use Cases |
| 4.5 | Project 3 | **Guided build (local Docker):** Simulated fleet IoT producer → Kafka topic → Postgres sink → Metabase line chart (engine temp over time) | Streaming Project |

### Week 5: Pipeline Orchestration (Theoretical)
> **Objective:** Design a pipeline before building one: learners will be able to distinguish scheduling from orchestration, model a workflow as a DAG with realistic sequential, parallel, branching and fan-in dependencies, design backfills, quality gates, retries, fault isolation, alerting and SLAs for production, select tooling and a batch, streaming or hybrid pattern from requirements rather than popularity, and produce an operational readiness checklist for launch.

| Index | Lesson | Content Breakdown | Project/Quiz |
|---|---|---|---|
| 5.1 | Why Orchestration? | Data pipelines & use cases; architecture (ETL/ELT, Lambda/Kappa, event-driven); scheduling vs orchestration; workflow dependency patterns | - |
| 5.2 | Orchestration Concepts | DAGs & tasks; triggers (schedule/event/waits); backfills & idempotency | QUIZ 1: Days 1–2 Orchestration & Concepts |
| 5.3 | Orchestration Tooling Landscape | Platforms compared (Airflow, Dagster, Prefect, Step Functions, ADF, Composer); engines & storage; cloud monitoring & cost awareness | - |
| 5.4 | Designing Resilient Pipelines | End-to-end design checklist; retries, isolation, failure response; quality gates, SLAs, alerting tiers | QUIZ 2: Days 3–4 Tooling & Resilient Design |
| 5.5 | Case Study | Production-grade architecture (CDC, streaming vs batch, lake layers, orchestration, ops) | - |

### Week 6: Pipeline Management with Airflow
> **Objective:** Put the Week 5 design under an orchestrator: learners will be able to run Airflow 3 locally and explain its architecture against Airflow 2, author a scheduled DAG with task dependencies, connections, sensors and event-based triggers, and operate it in production terms — reading logs to diagnose failures, configuring retries against idempotent tasks, setting freshness expectations, and alerting in a way that is tied to ownership and impact.

| Index | Lesson | Content Breakdown | Project/Quiz |
|---|---|---|---|
| 6.1 | Introduction to Apache Airflow | What is Apache Airflow, Core Concepts (DAGs & Tasks), and Advanced Concepts (Sensors & XComs) | - |
| 6.2 | Setting up Airflow | Installing Airflow, Accessing the UI, and Configuring Connections | QUIZ 1: Days 1–2 Intro to Airflow & Setup |
| 6.3 | Pipeline Triggers | Scheduling (Cron), Sensors, and Event-based Triggers | - |
| 6.4 | Monitoring & Operating Pipelines | Airflow Logs, Retries, SLAs, and Alerting | QUIZ 2: Days 3–4 Triggers & Monitoring |
| 6.5 | Project 4 | **Guided build (local Airflow 3 + S3 landing):** CoinGecko ingest → S3 → Postgres bronze/silver/gold (pandas) → Metabase; schedule every 2 hours | Airflow Project |

**Module 3: Storage and Distributed Processing (Weeks 7–9)**
> **Module Objective:** Decide where data rests and transform it at scale. Learners leave able to select and justify a storage architecture from relational through NoSQL to lakehouse, model transformations declaratively in dbt with tests and lineage, and process, optimise, validate and stream data through Apache Spark.

### Week 7: Big Data Storage
> **Objective:** Choose where data lives and shape it once it is there: learners will be able to apply relational design, normalisation and ACID reasoning to operational data, choose between relational, document, key-value, graph and columnar stores for a given workload, position data lake, warehouse and lakehouse against each other on schema, cost and trust, and build a medallion transformation layer in dbt Core with tests and generated lineage documentation.

| Index | Lesson | Content Breakdown | Project/Quiz |
|---|---|---|---|
| 7.1 | Database Systems | Relational Databases, Normalization, and ACID properties | - |
| 7.2 | SQL vs NoSQL | MongoDB, Document Stores, and JSON querying | QUIZ 1: Days 1–2 Database Systems & SQL vs NoSQL |
| 7.3 | Data Lakes vs Data Warehouses | S3 vs Redshift/Snowflake, Schema-on-Read vs Schema-on-Write, ELT with dbt Core, Medallion in the Warehouse | - |
| 7.4 | Data Lakehouse Architecture | Delta Lake, ACID on Lakes, and the Medallion Architecture (Bronze/Silver/Gold) | QUIZ 2: Days 3–4 Lakes vs Warehouses & Lakehouse |
| 7.5 | Project 5 | **Guided build:** Refactor Project 4 transformations using dbt Core in PostgreSQL; implement tests and generate lineage docs | dbt Core Project |

### Week 8: Processing Big Data in Spark
> **Objective:** Process data that no longer fits on one machine: learners will be able to explain Spark's execution model — driver, executors, partitions, lazy evaluation, transformations and actions — manipulate DataFrames with filters, aggregations, joins and window functions in PySpark, and write a batch ETL job that enforces an explicit schema, separates rejected records and lands validated Parquet.

| Index | Lesson | Content Breakdown | Project/Quiz |
|---|---|---|---|
| 8.1 | Distributed Computing & Spark | Why Spark? Cluster architecture, Driver, and Executors | - |
| 8.2 | Spark Core Concepts | RDDs vs DataFrames, Lazy Evaluation, Transformations vs Actions | QUIZ 1: Days 1–2 Distributed Computing & Spark Core |
| 8.3 | Manipulating Data in Spark | Filtering, Aggregating, Joining, and Window Functions in PySpark | - |
| 8.4 | ETL in Spark | Extracting, Transforming, and Loading data using Spark Jobs | QUIZ 2: Days 3–4 Manipulating Data & ETL in Spark |
| 8.5 | Project 6 | **Guided build (local PySpark + S3 lake):** CoinGecko landing Parquet → Spark silver/gold Parquet on S3; optional Delta stretch | Spark Data Processing Project |

### Week 9: Advanced Spark Concepts
> **Objective:** Make Spark jobs fast, trustworthy and continuous: learners will be able to diagnose a slow or failing job from the Spark UI by reading DAGs, stages and task metrics, apply caching, persistence and partitioning deliberately rather than by habit, build null handling, schema validation and profiling into pipelines, and write a Structured Streaming job with event-time windows, watermarks and checkpointed writes.

| Index | Lesson | Content Breakdown | Project/Quiz |
|---|---|---|---|
| 9.1 | Optimising Spark | Caching, Persisting, Partitioning, and Shuffle Optimization | - |
| 9.2 | Spark UI | Debugging applications, Reading DAGs, and analyzing stages/tasks | QUIZ 1: Days 1–2 Optimising Spark & Spark UI |
| 9.3 | Data Quality in Spark | Handling Nulls, Schema Validation, and Data Profiling | - |
| 9.4 | Spark Structured Streaming | Micro-batches, Windowing, Watermarks, and integration with Kafka/Kinesis | QUIZ 2: Days 3–4 Data Quality & Structured Streaming |
| 9.5 | Project 7 | **Guided build (local):** Kafka fleet telemetry (Project 3) → Spark Structured Streaming (watermark + windows) → silver Parquet on S3 | Streaming ETL Project |

**Module 4: AI-Era Data Engineering (Weeks 10–11)**
> **Module Objective:** Extend the platform to the workloads that now depend on it. Learners leave able to build the feature, tracking and serving infrastructure that machine learning requires, and to use and govern AI tooling within their own engineering workflow.

### Week 10: Data Engineering for MLOps
> **Objective:** Serve the systems that consume data: learners will be able to locate data engineering responsibility across the ML lifecycle and name the failure points caused by unreliable pipelines, build and evaluate a Spark ML pipeline, design feature tables and explain offline versus online serving and point-in-time correctness, and track, register and batch-score a model with MLflow.

| Index | Lesson | Content Breakdown | Project/Quiz |
|---|---|---|---|
| 10.1 | Where DE Meets ML | The ML lifecycle, DE's role in feature engineering and data serving | - |
| 10.2 | Spark MLlib Essentials | Feature extraction (VectorAssembler, StringIndexer), Pipelines, and basic training | QUIZ 1: Days 1–2 DE Meets ML & Spark MLlib |
| 10.3 | Feature Stores | Feature store concepts, using the Data Warehouse as a feature store, and tools like Feast | - |
| 10.4 | MLflow & Model Lifecycle | Experiment tracking, Model Registry, and automating deployment/retraining pipelines | QUIZ 2: Days 3–4 Feature Stores & MLflow |
| 10.5 | Project 8 | **Guided build (local):** Feature table from gold CoinGecko data → Spark ML Pipeline → MLflow tracking + registry → batch predictions Parquet | MLOps Project |

### Week 11: AI-Powered Data Engineering
> **Objective:** Work alongside AI rather than around it: learners will be able to distinguish AI used by data engineers from data engineering built for AI systems, apply CI/CD, data contracts and continuous training as DataOps practice, prompt and manage context well enough to review AI-generated data code with justified scepticism, and explain MCP, embedding pipelines, open table formats and data mesh as the directions the field is moving in.

| Index | Lesson | Content Breakdown | Project/Quiz |
|---|---|---|---|
| 11.1 | AI in Data Engineering | AI in DE vs DE for AI, GenAI Evolution, and RAG/Agents | - |
| 11.2 | DataOps Integration | CI/CD for Data, Data Contracts, and Continuous Training loops | QUIZ 1: Days 1–2 AI in DE & DataOps |
| 11.3 | GenAI for Development | Prompt Engineering (R-C-T-C), Context Management, and MCP | - |
| 11.4 | Future Trends | Unstructured Data (Vectors), Open Table Formats (Iceberg), and Data Mesh | QUIZ 2: Days 3–4 GenAI & Future Trends |
| 11.5 | — | **Review week** — no quiz or project; optional reading and recap | - |

**Capstone (Week 12)**
> **Module Objective:** Prove the whole thing works without a guide. Learners leave with a portfolio-grade platform they architected themselves, and with the ability to defend its design to an audience that did not build it.

### Week 12: Real-World Capstone Project
> **Objective:** Build and defend an end-to-end platform independently: learners will be able to architect, build and secure a production-style data platform for a self-chosen Kenyan-industry problem, integrating multi-source ingestion, a dbt ELT layer, Airflow orchestration, secrets and access control, failure alerting and a working AI component, and communicate the architectural decisions behind it in a 10-minute technical walkthrough.

| Index | Lesson | Content Breakdown | Project/Quiz |
|---|---|---|---|
| 12.1 | Capstone | **Independent build:** Architect a production-grade data platform solving a real-world Kenyan industry challenge. Requirements include multi-source ingestion, dbt ELT, Airflow orchestration, security controls, and an AI integration, culminating in a 10-minute technical presentation. | Capstone Project |
