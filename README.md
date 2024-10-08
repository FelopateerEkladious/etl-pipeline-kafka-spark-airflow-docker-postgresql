# Full-fledged ETL data streaming pipeline
## Overview
**Data Streaming**: The data first gets streamed from an API into a Kafka topic.

**Data Processing**: After that, a Spark job consumes the data from Kafka and transfers it into a PostgreSQL database.

**Orchestration with Airflow**: Airflow is used to coordinate both the data streaming and the Spark processing. In a real-world setup, the Kafka producer would continuously listen for API data. However, for demonstration purposes, we’ll schedule the Kafka streaming task to run once a day. After the streaming finishes, the Spark job kicks in, processing the data and preparing it for use by the LLM application.

All components will be set up and executed using Docker, with docker-compose managing the setup.

Tools and Technologies Used:
* Kafka
* Spark
* Airflow
* PostgeSQL
* Docker

![image](https://github.com/user-attachments/assets/dee974bb-a390-476d-9db4-d838e28068f4)
