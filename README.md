# My Journey to Becoming a Software Engineer

Within this repository, I will document my evolution as a software engineer. Maintaining a record of our progress is invaluable.
When I first embarked on my programming journey, I envisioned a way to reflect on my past decisions.
This repository stands as a testament to that vision, a chronicle of my growth in the world of software engineering.

## Programming Changes My Life

### Day 1883: Deprecation

Today I read the Software Engineering at Google deprecation chapter. This chapter is about how to deprecate a feature or an entire software product. Google have a clear view that if you don't deprecate a system two things can happened, the system will be expensive in maintenance and the system will be forgotten. In my work currently we are working into deprecate some applications for a new one, the process is not easy and requires a lot of time and effort.

### Day 1882: Continue Reading and LLMs

Today I continue reading the Software Engineering at Google book, I completed the testing part and started with the Deprecation section. Also in the work I attended some class room sessions related with AI and LLMs, I learned about the RAG concept explained by other amazing developers, I love learning listening to other developers, I think that is a good way to learn and share knowledge.

### Day 1881: Reading and Regression Testing

Today I learned about Regression testing. Regression testing involves executing tests to ensure the system continues to work after changes, such as bug fixes or new features, are applied. The problem with regression testing is when it’s manual, manual regression testing is time-consuming, the time is linear depending on the number of features/components to test and the journeys (the scenarios to test like adding a new user, buying a product, etc). We can express the human time required with the next formula: T = k * S * J, where k = the required time to test a journey, for example, 1 hour, S the number of components like 10, and J the number of journeys like 20. Using that example, we can say that testing a system with 10 components and 3 journeys for every component with a duration of 10 minutes per journey, we require 300 minutes to test the system. This is a lot of time and for this reason, automated testing is better. I continue reading the Software Engineering at Google book, reading the test part for me is very interesting.

### Day 1879-80: Larger Tests

Today I learned for Google what is a larger tests, for Google a larger test is a test in which many components interacts, a component can be a backend server, web server, database, etc. The idea of a larger test is to test the system as a whole, having the same dependencies like the production environment. Larger testing for Microservices can be a challenge depending of the number of Microservices involved because for each Microservice added to the application, the tests can increase exponentially. Is interesting how google require unit testing, integration testing and larger testing for any software developed, testing in Google is a must to do for any write code.

### Day 1878: Test Doubles, Stubs and Mocks

Today I studied testing techniques used to create unit tests that have external code dependencies. Test doubles are objects used to replace real objects implementations, a test double needs to follow the same API and have a similar behavior to the real object. Stubs most of the time are created with test libraries like Mockito for Java, create a unit test with stubs is very easy and fast. The trade-off about stubs is cause brittle tests and most of the times are not good to test behavior because if the code behavior changes, you will need to change the tests to mimic the new behavior. Finally, Mocks is normally used when you don't want to have a test double or code a real object. You can mock any object following dependency injection pattern. Be aware of these testing techniques is a good tool for any developer, testing is an important part in Software Engineering.

### Day 1877: Unit Testing Good Practices

Today, I read the Software Engineering at Google book. I learned about some interesting unit testing practices like Behavior Test Driven Development (BTDD). This approach focuses on testing the behaviors of the system rather than implementation details. In the past, I always thought that a method/function equaled unit tests. I now agree that testing this way causes brittle tests and many errors when the code changes. Another good practice is to create complete and concise tests. This means the test needs to have a good name and be comprehensive. You might think about creating objects in a separate method, but sometimes this is a bad practice because it hides the test complexity. The book has four chapters dedicated to testing. Google really loves testing in software.

### Day 1876: Airflow Certification

Today in the morning I presented the exam to get my [Airflow Fundamentals certification](https://www.credly.com/badges/a9a175e6-e7c0-45ea-8628-cf932d729a55). The exam was good, I passed with a 84% score, I am very happy because I studied a lot about Airflow to pass the exam, I feel very tired because I decide to take this certification due to the free opportunity to take the exam while studying for another two cloud certifications (AWS and IBM). I don't want to be in the same situation again, the next I think twice before take three certifications at the same time 😅. Now I am more relax and I can focus on continue developing some DAGs and my other studies topics.

### Day 1875: Spark Issues with Parallelism

Today I ws working on a Spark issue related with parallelism. I was working with a data pipeline that reads the data from a parquet file, next apply some modifications to this data to finally save the data into the same location with overwrite mode. The problem was an error happens while saving the data into the location, the reason error was Spark while spark is reading the data from the file another workers are removing and saving the data in the same location like a race condition. The solution was create a cache for the RDD and next from that cache saved the data to the location. This issue was very crazy because I have been working on that for more than 6 days.

### Day 1874: Completed Airflow 101 Course

Today I completed the [Airflow 101 Learning Path](https://academy.astronomer.io/path/airflow-101). I completed this course to prepare for the Airflow Fundamentals exam. I learned the basic of Airflow and some advances concepts, I think that I am ready for the exam, and I will take the exam in the next days.

### Day 1873: Continue with Airflow Sensors

Today I continue studying about Airflow [Sensors](https://airflow.apache.org/docs/apache-airflow/stable/_modules/airflow/sensors/base.html#BaseSensorOperator). I created examples DAGs to test the sensor functionality.
I learned that by default sensors have a timeout of 7 days to wait for the condition to be true, this can be a problem for some use cases,
also the poke_interval by default is 60 seconds. Sensors are a good feature to wait that something happen to perform another action. I want to create a pipeline
that implements sensors but for the moment I don't have an idea about what can I do with sensors.

### Day 1871-72: Airflow Sensors & Debugging

On Saturday I continue studying the Airflow 101 course, I learned about how works Airflow sensors, sensors are a way to wait for a condition
to be true before continue with the next execution task, is like waiting that something happens before continue with the work, for example:
wait for a file to be created in a directory, wait for a HTTP request to return a 200 status code, etc.
I also I learned some debugging DAG techniques for the most common problems in Airflow, like the DAG is not running because the scheduler is not running or in busy
processing other tasks, the DAG is not running because the start date is in the future, the DAG is not running because the schedule interval is not correct, etc. 

### Day 1870: Airflow XCOM Values Sharing Data Between Tasks

Today I learned how to share data between tasks in Airflow using XCOMs. XCOMs values are like having two functions and function B uses the returned value from function A. XCOMs values is a good way to share data between tasks, but is not recommended for share large amounts of data. Depending of the database you are using as a meta-database is the maximum size of the XCOMs values, for example if you are using SQLite you can share values with 2gb of size. Also the values shared by as XCOMs needs to be JSON serializable. 

### Day 1869: Filtering Parquet Files and AWS

Today I practice multiple ways to filter a DataFrame with PySpark and Python. I needed to do this because I need to remove from a DataFrame some not desired records, I learned how to filter using pyspark operations like `where` and `filter` using pyspark functions like `col`, `equal`, etc, also I create a temp view in Spark to apply the filter using SQL syntax, I discovered later that if you use `df.filter()`, you can pass the SQL query in string format as argument for the `filter` method. The pyspark flexibility to perform this operations is good but having multiples ways to do the same operation sometimes is a challenge because you are always looking for new ways to do their operations.

### Day 1868: JOIN left_anti in Spark and Airflow

Today I learned how the **left anti** join works in SQL and Spark. I needed to clean some data within a Spark dataframe using
a JOIN, I needed to use a JOIN because for filter a dataframe I need to use another DF to know the ID records to clean.
I have problems to understand how the left anti join works, but with practice and drawing I can complete the task
[spark-tutorial]("https://sparktpoint.com/spark-sql-left-anti-join/").  In other topics I continue working on my
Airflow certification today.

### Day 1866-67: Creating DAGs and IBM Cloud Advocate

On Monday I finished a DAG that generates a random user every 5 minutes and save the user in a PostgreSQL database, for the moment the database have 31920 records,
I have the plan to save the records in a CSV file and upload the file in hugging face to share the data. In other topics I completed 5 practice tests for the IBM Cloud Advocate Certification
achieving a general score 90%, I am happy with my current knowledge about IBM cloud.

### Day 1865: Problems Between Airflow Environments

I am having problems maintaining synchronized my two Airflow environments. I execute Airflow with pip in my development environment (Personal Laptop), and I execute Airflow with Docker in my server, for an unknown reason when I configured a Git repository to have my two environments sync, I have problems with the docker environment. I am going to debug the issue tomorrow and maybe consider execute both environments in the same way.

### Day 1864: BashOperator in Airflow and Building DAGs

Today I learned how the Bash operator works in Airflow. The BashOperator is used to execute Bash commands or scripts on the host machine where Airflow is installed, this means maybe you want to save the content of a HTTP request in a file on disk, with the BashOperator you can create a script to do this action and save the file in the /tmp directory as an example. I also created a DAG to understand how the BashOperator works. My first task is to execute a bash script to make an HTTP request and get a JSON file, the second task is to debug if the file was saved correctly, and the third and final task is to upload the content of the JSON file into a MongoDB collection. I could not configure MongoDB with the Mongo provider, I will have to continue configuring the connection tomorrow.

### Day 1863: Dag Development in Airflow

Today, I continued studying more about Airflow. I refresh my knowledge in Airflow concepts like a DAG run is the instance of a entire DAG that was executed and a Task Instance is an instance of a Task that was executed, remember a DAG can be composed from one or more Tasks. Tomorrow I have the plan to continue studying my Airflow course and finish the prerequisite course to start with the exam.

### Day 1862: Continue with AWS Practice Exams and Creating a Bash Script

Today, I continued doing practice exam for the AWS certification, in other topics I write a bash script to perform an action every ten minutes in an infinite while loop, the idea was avoid execute the command that triggers another process every time when the process is completed, with this way the script attempts every ten minutes execute the process.

### Day 1861: IBM Cloud Advocate Certification

Today, I continued studying for the IBM Cloud Advocate certification. At the moment, I am focusing on answering quizzes for this certification. I needed to revisit this study because the exam is scheduled for the last days of November or the first days of December.

I feel tired—why? Because I am working on achieving four certifications simultaneously:

1. IBM Cloud Advocate  
2. AWS Cloud Practitioner  
3. [Airflow Fundamentals](https://academy.astronomer.io/astronomer-certified-apache-airflow-core-exam)  
4. [Airflow DAG Authoring](https://academy.astronomer.io/astronomer-certification-apache-airflow-dag-authoring)  

The last two were not originally planned in my schedule, but I received a coupon to take both for free (with a 30-day expiration). I have organized a schedule to study for these certifications on specific days to avoid burnout and as a study technique. I’ll share more details in the future if this strategy proves effective. But please avoid work in multiple software certifications 😅.

### Day 1860: Airflow

Today I continue studying about Airflow, I am working in the next Airflow [course]("https://academy.astronomer.io/path/airflow-101").
I obtained the Airflow Fundamentals Exam free with a promotion, so I am studying Airflow to get the **Airflow Fundamentals Certification**.
I will need to pause my other current certifications because this promotion has a 30-days expiration time, so I only have 30 days to study and prepare for the exam.
  
### Day 1859: AWS and Testing Techniques

Today I continue with the AWS practice exams, for the moment I am getting better exam results, the key is to memorize the service definitions to match a use case with a definition.
For the Software Engineering at Google book I continue reading the testing book part, the book have 4 chapters dedicated to testing, looks like Google loves good software tested.

### Day 1858: Creating a new Repository and Continue with PostgreSQL

Today I created a new GitHub repository to store my Dockerfile and docker-compose files. The idea behind this repository is to have all my container files in one place because I have several Dockerfiles in my personal computer and my two Linux servers. I love to work with Docker and set up my own resources like databases, message brokers, etc., in containerized environments. You can find the repository in the next [link]("https://github.com/pablohdzvizcarra/personal-docker-library"). Also, I continued working on configuring my PostgreSQL database. I was working on setting up a separate container to create a backup of my database every day and store the backup in my server’s disk drive.

### Day 1857: Setting Up PostgreSQL Database and Airflow DAG Development

Today I worked into setting up a PostgreSQL database with Docker. I create a docker compose to deploy a PostgreSQL with special configurations, I was learning about the best ways to deploy and manage this database within a container, with configurations for performance, security and health checks. I created and configure the PostgreSQL database to save some data from my Airflow DAG into the database.

### Day 1856: Airflow DAG and Continue With AWS Practice Exams

Today I continue working on my Udemy course about practice exams by the AWS Certified Cloud Practitioner exam. Also I was working into my Airflow DAG, for the moment I am configuring the DAG to load the extracted data into a PostgreSQL database.

### Day 1855: Airflow, Google Testing Blog and Beyonce Rule

Today I discovered some amazing things reading the Software Engineering at Google book, I have been reading the chapter of testing at google, looks like testing in google is a mature process and is required that any engineer working on Google work with a test methodology. I discover the Google Testing Blog a good place to find useful information about testing, also I learned the Beyonce rule for testing `If you liked it, then you § put a test on it`, this rule is amazing xD. In other words I continue with my DAG development in Airflow.

### Day 1854: Working on the Udemy Practice Exams Course

Today, I continued working through the Udemy course and completed practice test number 3. Unfortunately, I didn’t pass, scoring 61% (the minimum passing score is 70%). I struggled particularly with questions related to Billing & Pricing and Cloud Concepts. The challenge with AWS is that it has so many services, making it difficult to remember all of them. Since I don’t work with AWS services in my daily activities, it’s harder for me to recall the most common service usages and descriptions. I’ll need to keep practicing and studying to feel fully prepared for the exam.

### Day 1853: Code Documentation

Today reading the Software Engineer at Google book, I review an important topic in software engineering Documentation. Documentation focusing on software products and code
is one of the most important aspect of good code, when you write good documentation for your API code, is easy for a user understand how your code works and the things that the code do.

### Day 1852 Studying for AWS Cloud Practitioner Exam

Today I continue working in the 6 Practice Exam | AWS Certified Cloud Practitioner Udemy course. I completed two of the six practice test.
The first was completed with 82% grade and the second with 72% grade. The minimum to pas the exam is 70%, really this exam is a little crazy, AWS have a lot of services to Studying
the idea is study the most important services and have luck like a coding interview in which you know how to solve a good number of problems waiting for find that problems in your coding interview.

### Day 1851 Continue with AWS and Reading

During this day I only studied a brief time for my AWS certification, for the moment I am only focusing on solving example exams to practice for the real, I completed the required courses. I have been reading the Software Engineering at Google book, for the moment in chapter 10. Documentation.

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
**Day 1801 - 1850 Java | Python | Airflow | AWS Cloud Practitioner | Data Engineering** [here](./day1501-2000/day1801-1850.md)</br>
