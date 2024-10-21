# My Journey to Becoming a Software Engineer

Within this repository, I will document my evolution as a software engineer.
Maintaining a record of our progress is invaluable.
When I first embarked on my programming journey, I envisioned a way to reflect on my past decisions.
This repository stands as a testament to that vision, a chronicle of my growth in the world of software engineering.

## Programming Changes My Life

### Day 1830-31-32-33-34-35-36-37: Back from Being Sick

I am back after being sick. During the last week, I had a severe bronchitis and couldn't code, so I needed to rest in bed. I didn't want to be sick, especially since my wife prohibited me from using my computer to code (to be able to rest). At least I finish to read the Everything is Fcked* book, which I found to be an amazing book.

On another note, today I resumed my AWS studies. I focused on networking services like VPN, Security Groups, Subnets, ACLs, Internet Gateway, and more. I also made some progress on my Airflow DAG. My goal is to create a DAG to process data, extract keywords from it, and update a SQL database with the extracted keywords.

### Day 1829 Ubuntu Server Maintenance

Today, I performed maintenance activities on my Oracle server running Ubuntu, upgrading it from 20.04 to 22.04 Jammy Jellyfish via SSH. During the process, I cleaned up cache, removed conflicting repositories, upgraded packages, and optimized my Docker environment.

I also set up a PostgreSQL database in Docker to practice SQL commands. While doing so, I noticed that my server was outdated and cluttered with unnecessary files, prompting a thorough cleanup. It was satisfying to get everything back in order!

### Day 1828 Big Data Foundations

Today I did a little course (3 hours) to learn some Data concepts, the course teach you Big Data concepts like what is big data, the 5Vs' in big data velocity, veracity, variety, volume and value. I learned interesting things about big data and data engineering like the Map Reduce operations, how a HDFS works.

### Day 1827 Java Code Issues

Today I worked into modify some Java code to change the way in which Deserialize some JSON data into a Java Objects.
The code use Google gson for the deserialization process, the code changes was fast, but the problem was the testing phase,
the application don't have unit testing, so the unique way to test the code changes is running the application entirely.

### Day 1826 Certificates and RabbitMQ

Today I worked in a hard task, I worked into renew some certificates for a RabbitMQ server, was amazing because I needed to generate
the certificates multiples times because sometimes was wrong generated. For me work with certificates and things related with security is funny and interesting but my knowledge on these topics is little.

### Day 1825 EC2, AutoScaling Group and ELB

Today I studied these AWS services and learning multiple things about them related with AutoScaling and Availability.
ELB is an amazing service to automatically scale up or down another services like Amazon EC2, normally ELB is used with the Auto Scaling service
to automatically apply scalability to an EC2 instance like applying the same technique in Kubernetes with a pod with three replicas.

### Day 1823-24 Continue with AWS Certification and Scheduling my Life

I continue working in the AWS Cloud Practitioner Essentials course from Amazon. This course is to complement my knowledge in AWS and
continue learning and practicing more. In other topics, during this month also I will need to work in an University onboarding course.

### Day 1817-18-19-20-21-22 Completed Udemy AWS Course

During these days I completed the Udemy Ultimate AWS Certified Cloud Practitioner CLF-C02 course. I continue working on my AWS Cloud Practitioner certification and learning about Cloud Computing in general. Also I learned the NIST definition about what is Cloud Computing, the Essentials characteristics, the service model and deployment models.

### Day 1815-16 Continue with AWS Certification

Over the weekend, I continued studying for the AWS Cloud Practitioner certification. I'm working on the final parts of the course to prepare for the exam. Today, I studied the AWS Well-Architected Framework, which helps create a cloud environment that follows enterprise and best practices. AWS has many cloud services, which can be frustrating as it's hard to grasp the basics of each one.

### Day 1814 Reading Software Engineering at Google book

Today I continued reading the software engineering at google book. I learned about how google measure the productivity using the GSM (Goal, Signal and Metric) methodology. A goal can be improve security in the code, the signal can be how much vulnerabilities are detected in the code and reduce the number of code vulnerabilities introduced in the new code, how do you when the goal was completed? well get a setup and review if the expected metric was achieved. It's interesting how Google some really ambiguous problems with good methodologies and achieve great results.

### Day 1813 Learning Other Data Processes Tools

Today I was investigating other data processing tools like Beam and Flink. Working with Airflow is good, but the problem is require a lot of resources to setup and run an local Airflow environment with Docker, so I am looking for alternatives like creating my pipeline with Apache Beam and package into a container to be executed in my Kubernetes cluster as a cronjob with Java obviously, also I want to learn Data Engineering with Java, I know Python is good but Java is better (my personal opinion).

### Day 1812 Continue with Airflow DAG

Today I continue working on my Airflow DAG, most of my time today was used to read some blogs from Netflix and also watch some youtube videos about data engineering. I am looking for an alternative to Airflow but to work with Java code, Python is great but is consuming a lof of my compute resources.

### Day 1811 Working with Spark in Airflow

Today I can't create a Spark session from an Airflow DAG to my local Spark cluster, I have various problems with this approach related with my Airflow cluster is working in a container environment, and my Apache Spark is installed locally in my machine. In the Udemy course that I did last week, I learned how to run a task with the Docker operator in a container environment, and running the task in a container environment is a good way, the problem with this approach is that we can't share data between the tasks in this way.
Well, I will have to continue investigating how to solve this problem and learn different ways to work with Spark and Airflow.

### Day 1810 Another DAG

Today I created a Airflow DAG to extract some JSON data from an open API using the HTTP operator, also I created a another DAG to monitor the pull request created into a  GitHub repository, if the commit messages have some pattern, the DAG is executed and print some elements in the console. Building these basics DAGs is helping me to understand Airflow concepts and practicing Python and Airflow.

### Day 1809 Studying Apache Airflow

Today I continue studying about Apache Airflow. I spend some time setup an Airflow environment in my MackBook only with pip and using the Airflow pip package, running Airflow in this way works at the first time, but starts to fail with the time and I don't know why, investigating more about the issues I discovered that configure an Airflow environment with pip is not recommended and complicated, well at the end I continue executing Airflow in my local machine using the astro CLI tool from Astronomer. I completed the [Astronomer Get started wih Airflow tutorial]("https://www.astronomer.io/docs/learn/get-started-with-airflow") in which I learned how to configure the local environment very easy with the astro CLI tool and also learn some new concepts about Airflow.

### Day 1807-08 Setup Airflow and Spark

I have been installing, setup and configuring Apache Airflow and Spark in my personal server to start developing DAGs in a production environment. I installed Airflow and Spark following the official documentations with Docker, really was hard configured both applications to be able to use in my Ubuntu server. I am going to start some data pipelines to create datasets and publish them in Hugging Face.

### Day 1806 Backfill dagruns in Apache Airflow & Hugging Face

Today I studied how to execute a DAG in Apache Airflow for a specific date, this process is calling backfilling. Imagine that you change your DAG and you want to execute your old DAG executions with these new features, well with backfill you can rerun the DAG for a specific date. Also I was looking the Hugging Face website, I want to create a dataset to store the stock information about the FAANG companies.

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
