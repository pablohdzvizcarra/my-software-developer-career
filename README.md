# My Journey to Becoming a Software Engineer

Within this repository, I will document my evolution as a software engineer.
Maintaining a record of our progress is invaluable.
When I first embarked on my programming journey, I envisioned a way to reflect on my past decisions.
This repository stands as a testament to that vision, a chronicle of my growth in the world of software engineering.

## Programming Changes My Life

### Day 1805 Visualizing Data in Metabase

Today I fixed the issue when loading the data from a Minio bucket to a PostgreSQL database, I configured wrong the connection in the Airflow connections section. When I upload the data to PostgreSQL I used Metabase to visualize the data, Metabase is a powerful tool to visualize data in a simple way, I created a dashboard to visualize the data that I uploaded to the database. I configured to visualize the historical data of the stock price of IBM company and also the current price for the stock.

### Day 1803-04 Docker Operator and Astro

I learned and executed a task inside a Docker container. Airflow has a DockerOperator that allows you to run a task inside a Docker container, this feature is very useful to execute task in an isolated environment and avoid install dependencies to Airflow only to be used one time. I am working into load a CSV file in a Minio bucket to a PostgresSQL database with the astro library, I am having some problems attempting to connect to the Minio bucket to download the file. I am going to continue working on this task tomorrow.

### Day 1802 DAGs, Task, PythonOperator in Airflow

Today I continue studying Apache Airflow, I continue learning about how to create DAGs creating some basic examples to make simple data pipelines, A DAG in Airflow contains N number of tasks, this task needs to be executed in a step order and also a task can't have a dependency with a previous task. in Airflow if you have a DAg with 10 task you can execute only one task standalone with the CLI, this is a good way to test the execution of a task.
PythonOperator in airflow is a way to execute a python function as a task, two main arguments are necessary to create a PythonOperator, task_id and python_callable, task_id is the name of the task in airflow and python_callable is the function that you want to execute as a task.
My first impressions about airflow are very good, I am developing a data pipeline to extract financial stock data from Yahoo Finance using web scraping and next upload the extracted data into a Database for the moment I don't know if use a SQL or NoSQL database to store the information.

### Day 1801 Continue with AWS Certification

Today I continue studying for the AWS Cloud Practitioner certification. I studied some AWS service like Application Migration Service, DataSync, Step functions, Ground station, Migration Hub, etc.

**Day 1 - 50 HTML - CSS - Javascript** [here](./day0-500/day0-50.md)</br>
**Day 51 - 100 Javascript** [here](./day0-500/day51-100.md)</br>
**Day 101 - 150 Javascript** [here](./day0-500/day101-150.md)</br>
**Day 151 - 200 Javascript** [here](./day0-500/day151-200.md)</br>
**Day 201 - 250 Javascript and start React JS** [here](./day0-500/day201-250.md)</br>
**Day 251 - 300 Javascript - React JS** [here](./day0-500/day251-300.md)</br>
**Day 301 - 350 Javascript - React JS and start Node JS** [here](./day0-500/day301-350.md)</br>
**Day 351 - 400 Start learn MERN stack** [here](./day0-500/day351-400.md)</br>
**Day 401 - 450 MERN stack - Docker - Typescript - TDD** [here](./day0-500/day401-450.md)</br>
**Day 451 - 500 Object Oriented Programming** [here](./day0-500/day451-500.md)</br>
**Day 501 - 550 Data Structures and Algorithms** [here](./day501-1000/day501-550.md)</br>
**Day 551 - 600 Java**</br>
**Day 601 - 650 Java** [here](./day501-1000/day601-650.md)</br>
**Day 651 - 700 Java and Spring Boot** [here](./day501-1000/day651-700.md)</br>
**Day 701 - 750 Java | Spring Boot | MySQL** [here](./day501-1000/day701-750.md)</br>
**Day 751 - 800 Java | Spring Boot | MySQL** [here](./day501-1000/day751-800.md)</br>
**Day 801 - 850 Java | Spring Boot | OCI** [here](./day501-1000/day801-850.md)</br>
**Day 851 - 900 Java | Design Patterns** [here](./day501-1000/day851-900.md)</br>
**Day 901 - 950 Java | Design Patterns** [here](/day501-1000/day901-950.md)</br>
**Day 951 - 1000 Java | Design Patterns** [here](./day501-1000/day951-1000.md)</br>
**Day 1001 - 1050 Java | New Job** [here](./day1001-1500/day1001-1050.md)</br>
**Day 1051 - 1100 Java | Python | Cloud Computing** [here](./day1001-1500/day1051-1100.md)</br>
**Day 1101 - 1150 Java | Containers | Cloud Native Development | OpenShift** [here](./day1001-1500/day1101-1150.md)</br>
**Day 1151 - 1200 Java | Containers | Python | Security** [here](./day1001-1500/day1151-1200.md)</br>
**Day 1201 - 1250 Java | Python | Security | English** [here](./day1001-1500/day1201-1250.md)</br>
**Day 1251 - 1300 Java | Python | Security | English | Soft-Skills** [here](./day1001-1500/day1251-1300.md)</br>
**Day 1301 - 1350 Java | Python | Spark | Microservices** [here](./day1001-1500/day1301-1350.md)</br>
**Day 1351 - 1400 Java | Python | Design Patterns | Microservices** [here](./day1001-1500/day1351-1400.md)</br>
**Day 1401 - 1450 Java | Design Patterns | CI/CD** [here](./day1001-1500/day1401-1450.md)</br>
**Day 1451 - 1500 Java | Design Patterns | CI/CD** [here](./day1001-1500/day1451-1500.md)</br>
**Day 1501 - 1550 Java | Python | Data Analytics | CI/CD** [here](./day1501-2000/day1501-1550.md)</br>
**Day 1551 - 1600 Java | Python | Data Analytics | CI/CD** [here](./day1501-2000/day1551-1600.md)</br>
**Day 1601 - 1700 Java | Python | ReactJS | Data Structures and Algorithms** [here](./day1501-2000/day1601-1705.md)</br>
**Day 1701 - 1750 Java | Go | DSA | A Common-Sense Guide to DSA Book** [here](./day1501-2000/day1706-1750.md)</br>
**Day 1751 - 1800 Java | Python | DSA | AWS Cloud Practitioner | Data Engineering** [here](./day1501-2000/day1751-1800.md)</br>
