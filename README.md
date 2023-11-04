# My Journey to Becoming a Software Engineer

Within this repository, I will document my evolution as a software engineer.
Maintaining a record of our progress is invaluable.
When I first embarked on my programming journey, I envisioned a way to reflect on my past decisions.
This repository stands as a testament to that vision, a chronicle of my growth in the world of software engineering.

## Programming Changes My Life

### Day 1486 Python Desktop App

Today, I successfully developed a desktop application for validating JSON schemas using Python and PyQt6.
I undertook this project with the aim of learning how to create desktop applications. Initially, I considered using Java for the task. However, considering I already had the Python code to create and validate JSON schemas, I opted for Python. The outcome was excellent, and the application fully meets the specified requirements. I am pleased with the result.

### Day 1485 OutOfMemory

Today, I started debugging a Java OutOfMemory error. Our application utilizes 2GB of RAM memory, but it's throwing an OutOfMemory exception because the heap space is full. Tomorrow, I plan to review the resource consumption of the application and pinpoint the part of the code where the memory is being exhausted.

### Day 1484 Deep Dive SFTP Protocol

Today I have been studied how works the SFTP protocol. I learned interesting things like the SFTP protocol runs on the SSH protocol, you need first creates a SSH connection and then a SFTP channel is open by the serves that manage the connection.
I did a basic diagram to understand the step under a SFTP connection and created a basic golang application to test a SFTP server running in a container.

### Day 1483 SFTP Server Issue

Today I had a SFTP connection problem, for some reason I cannot connect to a SFTP server using the JSch Java library, I attempt some solutions to fix the issue, but I cannot achieve the connection. The error is strange because I can connect to a SFTP server created with a container. Another application has the same code, use the same library and connect with the same library. Tomorrow I will need to continue investigating more about how an application creates a SFTP connection.  

### Day 1482 Linux users

Today I had a problem with a SFTP podman container, I created a SFTP server with a container the problem was the application that needs to read data from the SFTP server does not work. The application cannot find the files inside the container, I attempt to find a solution for the problem, but I cannot fix the issue. In the past when I needed to create SFTP servers in containers, working with docker is more easy, I have not this type of problems.

### Day 1480-81 Test-Driven Development

During the weekend I continued studying and practicing more about TDD methodology. I want to apply TDD for most of the code that I will need to write in the future, code for work and for personal projects.

### Day 1479 Craftsmanship

Today, I've decided to take a break from my Red Hat certification course and instead, devote my time to reading the '
Clean Craftsmanship' book. This book is something I'd started reading as a continuation of the 'Clean Agile' book.

During the week, I have been practicing TDD (Test-Driven Development). What surprised me about this technique is that it
has significantly reduced my impostor syndrome as it gives me a thorough understanding of the code. This knowledge not
only aids me while fixing a bug but also while adding a new feature, as it allows me to refactor the code efficiently.

### Day 1478 Image Layers

Today I studied about the image layers that are generated when you build a container with Podman/Docker. When you start
to create a container with a Dockerfile the first instruction **FROM** choice the base image layer for your container,
some instructions like RUN, COPY and ADD creates image layers, these images layers are thin and ephemeral and can be
reusable. Also, I learned that the image layers work in Copy-on-write operation.

### Day 1477 Containerfile Instructions

Today, I continued my study on creating containers. I utilized advanced instructions such as ENV and ARG to customize
container creation. By employing different instructions, you can personalize the process of container creation.

#### Day 1476 Containerfiles

Today I began the Red Hat certification path about Cloud-Native developer.
In the Cloud-Native developer certification I will need to improve and learn new skills about Java, Quarkus, Containers,
Kubernetes and OpenShift technologies. I choose this certification path because I love work with Java and DevOps
methodology. The course in large and hard.

#### Day 1475 Abstract Factory

Today I have been working in my Spark application to ingest data from a CSV file to a database. I implemented the
Abstract Factory pattern to change the database target without clean and write code. Using the Abstract Factory pattern
I can write implementations for save the data in different NoSQL databases like Cloudant and CouchDB.

#### Day 1473-74 Spark Ingestion App

Over the weekend, I've been working on creating a Java application using Spark to ingest data into a database. I've
encountered challenges with the volume of data involved - I was attempting to process a batch of two million records,
which the database was unable to handle. Consequently, I modified the Java code to split the data into manageable
chunks. However, a subsequent issue arose - the application failed after splitting the data, and was only able to upload
one million of the two million records.

#### Day 1470-71-72 Java and Python

These days I was working in write Python code create reports in PDF format, I have test data in many databases, so I
have been creating an ETL process to extract data from multiple sources, transform in a unique data and finally load the
data into CSV files. With Java, I am working in an application to create data database records to apply some query's to
these records.

#### Day 1469 Testing Database SLA

Today I created a basic Java application to test the SLA (Service Level Agreement) for a database.
The application works as a cronjob that every minute sends five requests to the database to save documents if an
error occurs when saving the data in the database.
We catch the error and try again to save the registry again.
The application runs in a Docker container in an oracle server to avoid wasting my resources on my laptop.

#### Day 1465-66-67-68 Finish Clean Agile

Recently, I completed reading the Clean Agile book. While going through its pages, I experienced several 'aha' moments,
realizing the essence of Agile in my work. It became evident that our current approach to Agile practices was lacking.
Prior to reading the book, I didn't fully grasp the concept of Agile. Now, armed with newfound knowledge, I am equipped
to apply Agile methodologies effectively in my daily work.

#### Day 1464 Clean Agile

Today I have been continuing reading the Clean Agile book, this book is amazing.
I love the next message about practice TDD:
We practice TDD because it gives us the courage to keep the code clean and orderly.
It gives us the courage to act like professionals.

#### Day 1463 Looking for More New Java Features

Today I am studying about the nex Java ecosystem like GrailVM and trying to build a native image. I had some
problems with maven about compiling the project, its amazing when you only use Spring Boot for all your projects,
how building an application from scratch can be arduous at the start.

#### Day 1462 Sealed Classes

Today I began to study the new features that arrive with Java 17 and Java 21, I am not studying about the new Java
features, and I have the goal to obtain the Java 17 Developer certification next year.

#### Day 1461 Kotlin Cronjob

Today I have been learning how to create a Cronjob application with Kotlin.
I will need to use a JVM library to create the cronjob functionality.
The application was easy only execute a short task every hour, the idea was created the application to run in a Docker
container.

#### Day 1458-59-60 Finish to Read Head-First Design Patterns Book

On the weekend I finished reading the Head-First Design Patterns.
It took me three months to complete it.
During my journey, I learned a lot about design patterns and Java.
I really love the Head-First books because they offer a lot of examples, and you can read the book in an interactive
way.
I learned some new things about Java and Design Patterns, and also gained more knowledge in Software Design principles
like SOLID principles.

#### Day 1457 Learning More About Design Patterns

Today I had been learning more about design patterns.
The last of the Head-First Design Patterns book talks about what is a pattern, what is a pattern catalog, etc.
I am learning general concepts about Design Patterns.
Also, I started a new book lecture, this time I choose the Clean Agile book, I am always trying to read two books at
the same time, one book related a code (read the book sitting in front of my laptop) and other book that I can read in
any place like the commute to my work.

#### Day 1456 Finish MVC Pattern Study

Today I completed my study of the MVC design pattern.
Now, I understand that the MVC pattern is intricately woven with other patterns such as Strategy, Observer, and Adapter.
I recall studying the MVC pattern during my exploration of Angular.
It fascinated me because Angular's framework incorporates this pattern at its core.

#### Day 1455 Studying the MVC pattern

Today I studied the Model-View-Controller (MVC) design pattern.
Now I know that the MVC pattern is composed of other patterns like the Observer and Strategy patterns.
I am building a Java Swing application following a book tutorial to understand the MVC pattern.
Learning about Java Swing is a pleasure for me because it is a great technology to create desktop applications.
Maybe when I finish this book, I will learn more about Java Swing.

#### Day 1454 Compound Patterns

Today I am creating a basic application following a tutorial.
The application implements six different design patterns like Adapter and Observer.
My next thing to study is MVC(Model View Controller) design pattern; I hope that this time studying the MVC pattern
will be less difficult that the other times and I can understand in a better way.

#### Day 1451-52-53 The Proxy Pattern

These days I continue to read the Head-First Design Patterns book.
The **Proxy** pattern is a great tool for our design box; I remember in the past that I could see some proxy
implementations, but I don't know that this type of implementing the code has a name.
Basic description: The Proxy pattern protects the access to an object and next surrogate the calls to the real object.

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
**Day 751 - 800 Java | Spring Boot | MySQL** [here](day751-800.md)</br>
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
**Day 1301 - 1350 Java | Python | Spark | Microservices** [here](day1301-1350.md)</br>
**Day 1351 - 1400 Java | Python | Design Patterns | Microservices** [here](day1351-1400.md)</br>
**Day 1401 - 1450 Java | Design Patterns | CI/CD** [here](day1401-1450.md)</br>
