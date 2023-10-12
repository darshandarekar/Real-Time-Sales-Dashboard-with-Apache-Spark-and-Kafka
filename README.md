# Real Time Sales Dashboard with Apache Spark and Kafka

## Introduction

This project implements a real-time sales dashboard using Apache Spark and Kafka, providing instantaneous insights into sales trends. It incorporates an efficient data pipeline, enhancing data visualization for quick decision-making. The following technologies are utilized:

- Apache Spark (Pyspark)
- Apache Kafka
- Django
- Chart.js
- Python

## Purpose

The purpose of this project is to create a robust, real-time dashboard that processes online orders data promptly, achieving a reduction in data processing latency. It involves the use of Apache Spark for data processing, Kafka for stream data simulation, and Django with Chart.js for building the dashboard.

## How It Works

1. **Real-Time Dashboard Application (Django):**
   - Navigate to the `realtime_charts` directory.
   - Activate the Python virtual environment.
   - Install required Python packages.
   - Create a MySQL database named `ecom_db`.
   - Run the Django server using `python manage.py runserver`.
   - Access the real-time dashboard at http://127.0.0.1:8000/.

2. **Kafka Producer Application (Stream data simulator):**
   - Navigate to the `kafka_producer_consumer` directory.
   - Install required Python packages.
   - Run the Kafka producer using `python kafka_producer.py`.

3. **Data Processing Pipeline (Spark Streaming):**
   - Navigate to the `realtime_data_processing` directory.
   - Submit the Spark job using the command:
     ```bash
     spark-submit --master local[*] --packages org.apache.spark:spark-sql-kafka-0-10_2.12:3.3.0,mysql:mysql-connector-java:5.1.49 --files /path/to/datamaking_app.conf /path/to/realtime_data_processing.py
     ```
   - Monitor the real-time dashboard at http://127.0.0.1:8000/.

## Installation

### Prerequisites

- Ubuntu 20.04 Linux OS
- Python 3
- MySQL
- Apache Hadoop 3
- Apache Spark 3.3.0
- Apache Kafka 3.2.0

- Follow the instructions in the provided text files to set up the project environment.

### Execution Steps

1. **Activate Python Virtual Environment:**
   ```bash
   source /path/to/venv/bin/activate
- Install Dependency Python Packages
```bash
cd /home/datamaking/workarea/code/course_download/ecom-real-time-case-study/realtime_charts
sudo apt-get install libmysqlclient-dev libssl-dev python3-dev
pip install -r requirements.txt
```

2. **Run Real-Time Dashboard Application:**

```bash
cd /home/datamaking/workarea/code/course_download/ecom-real-time-case-study/realtime_charts
python manage.py runserver
```
- Access the dashboard at http://127.0.0.1:8000/

3. **Run Kafka Producer Application (Stream Data Simulator):**

```bash
cd /home/datamaking/workarea/code/course_download/ecom-real-time-case-study/kafka_producer_consumer
pip install -r requirements.txt
python kafka_producer.py
```
4. **Run Data Processing Pipeline Application (Spark Streaming):**
```bash

cd /home/datamaking/workarea/code/course_download/ecom-real-time-case-study/realtime_data_processing
spark-submit --master local[*] --packages org.apache.spark:spark-sql-kafka-0-10_2.12:3.3.0,mysql:mysql-connector-java:5.1.49 --files /home/datamaking/workarea/code/course_download/ecom-real-time-case-study/realtime_data_processing/datamaking_app.conf /home/datamaking/workarea/code/course_download/ecom-real-time-case-study/realtime_data_processing/realtime_data_processing.py
```
- Keep monitoring the real-time dashboard at http://127.0.0.1:8000/.



