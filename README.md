# My Journey to Become a Software Engineer

In this repository, I will keep the progress of my career as a software engineer. I think it is very
important that we all have some record of our progress, when I started programming, I wanted to have
a record to go in the future and see what decisions I have taken and this repository is the result
of that record.

### Programming Changes My Life

#### Day 1351 Testing Spark Data Source

Today I continue building the data source implementation following the tutorial,
the tutorial does not have any unit testing, and I start to create some unit testing to understand the code in a better
way, the code is a very complex due to the complexity of the implementation, and well, I do not have high knowledge with
Spark.

#### Day 1350 Continues Spark Data Source

Really building your own data source to ingest data to Spark is a hard task,
but I am learning a lot about Java and technical concepts.
Imagine that you have three SFTP servers that contains I don't know maybe video files, and you need to collect the data
from these three servers about the name of the videos, duration,
time creation and more things, maybe your first approach is to build a Script that collects and parse the data for you
in
a JSON/CSV file, but with Spark and Java you can build your own implementation.
A very powerful tool to collect data.

#### Day 1347-48-49 Spark and Java

Well on the weekend I have been reading the Spark in action book,
currently I am in the part of the book in which I am writing a complicated code,
working at a low level with Spark interfaces and Java API.

#### Day 1346 Spark Data Source

Today I started to build my own data source to ingest data from Spark,
this is a hard and complicated task for me at this moment because of my little knowledge of the Spark technology,
but well, I am learning a lot of things about Java and study advance topics in the JVM world.

#### Day 1345 Java and Spark

Today I learn a lot about Java and how it works with ZIP files.
I learn how to compress and uncompress some ZIP files,
also I learn about what is good practice to read the content of a ZIP file into buffers and how is manage the data in a
low level (working with bytes).
In the afternoon, I need to learn how to deploy an Elasticsearch instance in a Docker
container and how to ingest some data using the REST API.

#### Day 1344 Spark and RDBMS Databases

Today I learned how to ingest data from a relational database to a Spark and create a dataframe with the data.
Also, I need to create a MYSQL docker container,
I had one problem because I need that the docker container has the Sakila database inside,
so I need to look for a docker image with the Sakila database loaded.

#### Day 1343 Big Data Formats

Today I have been studying about Big Data formats to storage information like Avro, Parquet and OCR,
also I do a little application parse CSV files to Parquet.
This is only curious because in the work we manage a lot of CSV files,
and sometimes we have problems with the CSv file size maybe we can change the format to storage the information,
formats more compressed that use less Megabytes of memory.

#### Day 1340-41-42 Spark

On the weekend I have been reading the "Spark in Action" book, working with files with Spark is easy because Spark
offers a lot of configured tooling to do the ingestion of data using some files (CSV, JSON, XML, etc.).
Well I continue focusing on Java and the JVM, today need to use the VisualVM tool to debug one application that consumes
a lot of memory in a Kubernetes Pod;
performance in applications is one of the things that you forget to learn in your daily work.

#### Day 1339 Groovy Scripting

Today I did two basic Groovy script one for create passwords and the other to create a Spark session, also I learn how
to configure a Scheduler in Java and Spring Boot, I have pending learning about concurrency with Java, on the weekend
I can advance in this topic.

#### Day 1338 Working with Spark Interactively

Today I have been studying how to work with a Spark cluster interactively. I have a Jupyter notebook with Spark
deployed on an Oracle server, which allows me to perform my testing activities in this cluster. Additionally, I learned
about the potential issues that can arise with Jar files in Java, and I discovered a new concept called "uber Java jar,"
which refers to a jar file that contains all the necessary dependencies. Tomorrow I will continue exploring Spark and
Java.

#### Day 1337 Spark and Java Lambda Functions

Today I have been studying how to write Spark functions using lambda expressions instead of creating separate classes
for each operation. Additionally, I have been exploring the Serialization and Deserialization process in Java. I've
often encountered Java classes that implement the Serialization interface, but I never took the time to ponder the
reason behind it.

#### Day 1336 Spark MapReduce Operations

Today I learned that Spark allows you to perform MapReduce operations with ease, abstracting away the complexity of
implementation.
I also discovered that the key concept behind MapReduce is its ability to execute operations in a distributed manner,
which proves extremely beneficial for handling big data. While reading about MapReduce, it reminded me of a past
instance where I struggled with a complex operation using a for loop, and I realized that MapReduce could have been a
valuable solution at that time.

#### Day 1333-34-35 Spark Lazy

On the weekend, I continued studying Spark, particularly focusing on understanding why Spark is considered "lazy." It's
truly fascinating how Spark can efficiently handle big data by creating jobs and tasks. Working with 7 million records
is remarkably fast. I'm eager to delve deeper into this topic as I believe this concept will prove valuable in the
future.

#### Day 1332 Continues with Dataframe

Today I studied a brief about how the dataframe is built. I learned the difference between a Dataframe and a Dataset,
it's curious about how Java called the dataframes, I feel a little sick, I hate when I have a cold, programming is
complicated with a cold.

#### Day 1331 Union Dataframes

Today I did a union with two dataframes also I learned how to modify the name of the columns and how to add more
columns in a dataframe, and fill the values in these columns.
Manipulates Dataframes with Spark sometimes can be a little tedious because you need to ensure that the type of the
value in the column is the same for the column to apply the union, well, I am happy because I am learning a new
technology (Spark), learning a little about new field in Computer Science (Data Engineering) and the best I am
learning all these things with Java, my main language.

#### Day 1330 Study the Dataframe

Today I have been studied about what is a dataframe and how it is built. I believe that this concept can be useful
in my daily work activities because in my work I use the Pandas Python library and pandas also manipulate the data in a
dataframe, tomorrow I continue studying and practicing with this concept with Spark and Pandas.
I remember one time when I need to use both libraries in the creation of a CSV report with Java code.

#### Day 1329 Spark Mental Model

Today I embarked on a new exercise: constructing a mental model of how Spark functions in tasks such as data ingestion,
transformation, and loading. This concept holds immense power, especially when grappling with complex ideas. Building a
mental model serves as a valuable tool for truly comprehending these concepts. I have always advocated for simplifying
intricate concepts through visualization and abstraction, as it proves to be the most effective approach to learning.

#### Day 1326, 27, 28

On the weekend, I took a break from learning about Microservices. I decided to start reading a new book about Spark,
possibly covering Scala or Java. In the end, I began reading "Spark in Action." Spark is an amazing technology, and
while I often use Python pandas for various tasks at work, I discovered that Scala is incredibly powerful. On Sunday, I
dedicated my time to deploying a Scala cluster on a Kubernetes cluster, but unfortunately, I was unable to achieve that.
However, I did manage to work with Scala using the Maven package.

Today is Monday, and I started the day with a quick exercise. I ingested data from a CSV file, added some additional
fields, and efficiently stored the entire dataframe in a PostgresSQL table. It was a straightforward and fast process.

#### Day 1325 Threading in Python

Today I need to study about threading in Python because I am building some scripts, and I need to improve the
performance; One script takes a long 3 minutes in execution, implementing parallelism and threading I want to reduce
a one minute.

#### Day 1324 Saga

Today I start to study the Saga pattern in Microservice architecture a Saga pattern has a lot of concepts that you
need to understand good to apply the Saga in a Microservice architecture, it looks like that I will continue
studying Saga for some days maybe a week, the book that I am reading dedicates a whole chapter to the Saga pattern.

#### Day 1323 Transactional Context

I realize the importance of revisiting the basics to grasp the concept of a transactional context. Despite encountering
the term frequently during my study of Microservices, I never truly understood its meaning. Therefore, I dedicated today
to performing a simple exercise on Java code to gain a better understanding of the context.

#### Day 1322 Discarding Duplicates Messages

Today I have been studying how to prevent the processing of duplicate messages in a consumer.
Let's say you have an OrderPay event, and due to some reasons, the broker duplicates the message twice.
It is essential to implement a mechanism to discard duplicate messages in the consumer before process it, ensuring that
the same message is not processed multiple times.

#### Day 1319-20-21 Continue Reading

On the weekend, I was reading the book "Microservice Patterns." Today I need to work on an exercise with Kafka, where
I'm trying to send a message with a shared ID. However, I'm facing some difficulties in configuring the Kafka cluster in
a Docker container, and as a result, I'm unable to complete the test. Perhaps I need to have a better understanding of
the basic abstractions and how Kafka works with Java code. I believe that taking this approach will help me gain a
clearer understanding of how things are built.

#### Day 1318 Continue Reading Messages Architectures

Today I had studied about broker and brokerless architectures in Microservice context.  
Also, I learn a good lesson, when you need to a high-process or a batch job, please think about the resources, the most
of the time developers never think in these things I maybe we can have problems when deploying the application in the
environment the classic works on my machine.

#### Day 1317 Broker and Brokerless Architecture

Today I finished my Kotlin project initialized yesterday.
I can fix the issue with the Kotlin test library and learn how to Spy objects in unit testing.
Today I start to study about the broker and brokerless architecture.

#### Day 1316 One-way Notifications

Today I have been learning the one-way notification message pattern, this message pattern it's easy to understand,
but I have some problems trying to implement in a basic program with Kotlin, I don't have good knowledge in Kotlin
and I don't know how it works the kotlin-test library for write unit testing, tomorrow I will continue implementing
this pattern and fix my issues with the kotlin-test library

#### Day 1315 Message Patterns

Today I have been working on learning message patterns in Microservices. I am familiar with Kafka, RabbitMQ, and the
concept of event architecture. It is interesting how simplifying things can help you grasp concepts more quickly. I
completed a small implementation where I applied a message pattern using Java/Python code. Tomorrow I will continue
studying this topic.

#### Day 1312-13-14 Self-improvement

On the weekend, I took a course on self-improvement focused on career management. Additionally, I started reading a book
on the same topic. I sometimes feel lost and need to recover from setbacks. Today, I am continuing to study English and
practice Python and data manipulation.

#### Day 1311 Work Management and Stack Overflow Survey

Today I participated in the Stack Overflow survey for 2023. This is the third year in a row that I have taken part in
this survey, and once it was completed, I eagerly read through the results. It's truly fascinating to see the responses
and insights shared by others.
In the afternoon, I dedicated my time to a course on work management available on the Harvard Manage Mentor platform.
Over the weekend, my plan is to practice and apply the knowledge gained from the course by completing exercises that can
be applied to my daily life.

#### Day 1310 Implementing Service Discovery Patterns

Today I dedicated my time to further enhance my understanding and proficiency in the 3rd party registration and
server-side discovery patterns. Through the implementation process, I followed the principles of Test-Driven
Development (TDD), which yielded satisfying outcomes. Notably, my testing skills have significantly improved, empowering
me to articulate pattern concepts more effectively by practicing with practical examples rather than solely relying on
theoretical descriptions.

Furthermore, I have a mentoring session scheduled for the morning.
While I feel slightly apprehensive about my English proficiency, I am determined to improve my language skills to
communicate more efficiently with English speakers.

#### Day 1308-09 Service Discovery

These days, I have been learning about Service Discovery. I have learned about various patterns such as
Self-Registration, Client-Side Discovery, 3rd-Party Registration, and Server-Side Discovery. Additionally, I have been
practicing implementing these patterns using Java code and applying Test-Driven Development (TDD). However, I feel the
need to dedicate more time to these patterns and engage in additional exercises, as I believe they are of great
importance and can serve as valuable tools in my repertoire.

#### Day 1307 Kubernetes

Throughout the whole day, I have been practicing Kubernetes. I have created several applications and configured a local
Kubernetes cluster to run them. My tasks have involved creating service resources to expose the applications and
ConfigMaps to add environment variables. For most of these tasks, I have relied on ChatGPT, which has proven to be a
valuable tool. However, one challenge I have encountered is understanding the underlying reasons behind the actions.
While I know how to perform certain tasks, grasping the "why" behind them can be more difficult. I believe that studying
books and reading official technology documentation would provide a better understanding of the underlying concepts.

#### Day 1304, 05, 06 ChatGPT and Python

On the weekend, I completed a course on using the ChatGPT API with Python and Jupyter Notebook.
The course was offered by deeplearning.ai, a reputable platform.
I gained valuable insights on creating effective prompts and utilizing various features of ChatGPT.
Additionally, I made progress in reading the "Microservice Patterns" book.

#### Day 1303 Learning Pandas

Today I am continuing learning more about pandas, I need to do a basic diagram showing some data using the matplotlib
python library also I learn how to select some date from a pandas dataframe.
I cannot advance in the Microservice Patterns book because I am continuing studying english.

#### Day 1302 Pandas and PySpark

Well, today I continue practicing with pandas and pyspark python libraries.
I need to analyze some CSV files and extract selected data.
Filter data with pyspark is like SQL, but with pandas I believe that is more efficient.
I do the same process with the two libraries, but with pyspark the process takes more time rather than pandas.
Also, saving a dataframe in a new csv is easier with pandas.

#### Day 1301 Pyspark

Today I learned how to read a CSV file using Pyspark and how to filter the rows in the CSV file with a condition.
Tomorrow I will need to investigate what are the differences between Apache Spark and Pyspark.
I can see that if I turn off my Spark Docker container on my local machine, Pyspark continues working without problems,
and this behavior is strange because what Spark process uses the pyspark library.
I do not know the answer to this question, but tomorrow I will review this.

**Day 1 - 50 HTML - CSS - Javascript**  [here](./day0-50.md)</br>
**Day 51 - 100 Javascript** [here](./day51-100.md)</br>
**Day 101 - 150 Javascript** [here](./day101-150.md)</br>
**Day 151 - 200 Javascript** [here](./day151-200.md)</br>
**Day 201 - 250 Javascript and start React JS** [here](day201-250.md)</br>
**Day 251 - 300 Javascript - React JS** [here](day251-300.md)</br>
**Day 301 - 350 Javascript - React JS and start Node JS** [here](day301-350.md)</br>
**Day 351 - 400 Start learn MERN stack** [here](day351-400.md)</br>
**Day 401 - 450 MERN stack - Docker - Typescript - TDD** [here](day401-450.md)</br>
**Day 451 - 500 Object Oriented Programming** [here](day451-500.md)</br>
**Day 501 - 550 Data Structures and Algorithms** [here](day501-550.md)</br>
**Day 551 - 600 Java**</br>
**Day 601 - 650 Java** [here](day601-650.md)</br>
**Day 651 - 700 Java and Spring Boot** [here](day651-700.md)</br>
**Day 701 - 750 Java | Spring Boot | MySQL** [here](day701-750.md)</br>
**Day 751 - 800 Java | Spring Boot | MySQL** [here](day751-800.markdown)</br>
**Day 801 - 850 Java | Spring Boot | OCI** [here](day801-850.md)</br>
**Day 851 - 900 Java | Design Patterns** [here](day851-900.md)</br>
**Day 901 - 950 Java | Design Patterns** [here](day901-950.md)</br>
**Day 951 - 1000 Java | Design Patterns** [here](day951-1000.md)</br>
**Day 1001 - 1050 Java | New Job** [here](day1001-1050.md)</br>
**Day 1051 - 1100 Java | Python | Cloud Computing** [here](day1051-1100.md)</br>
**Day 1101 - 1150 Java | Containers | Cloud Native Development | OpenShift** [here](day1101-1150.md)</br>
**Day 1151 - 1200 Java | Containers | Python | Security** [here](day1151-1200.md)</br>
**Day 1201 - 1250 Java | Python | Security | English** [here](day1201-1250.md)</br>
**Day 1251 - 1300 Java | Python | Security | English | Soft-Skills** [here](day1251-1300.md)</br>

