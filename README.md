# My Journey to Becoming a Software Engineer

Within this repository, I will document my evolution as a software engineer.
Maintaining a record of our progress is invaluable.
When I first embarked on my programming journey, I envisioned a way to reflect on my past decisions.
This repository stands as a testament to that vision, a chronicle of my growth in the world of software engineering.

## Programming Changes My Life

### Day 1687-88-89-90 Javascript, NodeJS and Synchronous Code

These days I have been remembering how to write Javascript code. I needed to refresh my JS knowledge because I started to work on a JS project, I have a problem remembering how works the async code with async/await, I needed to review again the [javascript.info](https://javascript.info/async-await) async/await tutorial, also remember how to write JS unit tests with [jest](https://jestjs.io/), on the weekend I have the plan to create an JS application to continue practice.

### Day 1686 Analyzing Linux File System

Today I continue reading the Linux book and making some exercises with linux command and Python code. I take the output of some Linux command like cat, sort and uniq, and analyze the output with python, and transform this text plain into CSV file to apply filtering operations.

### Day 1684-85 Completed Red Hat Course

On the weekend I completed the Building Kubernetes Application Red Hat course. This course has a 32 hours duration, I spend around three months to complete the course, because the course has multiple labs and exercises. I learned a lot of things in the course specially Containers and OpenShift.

### Day 1681-82-83 RedHat Course

These day I have been working in the [Building Kubernetes Application](https://training-lms.redhat.com/sso/saml/auth/rhopen?RelayState=deeplinkoffering%3D45314152) course, I am doing the last part of the course, my goal is finish this big and challenge course on the weekend to continue with a site project (a data analytics python application). One of my goals on this year is study Python, Data Engineering and learn a new programming language maybe Go or Rust.

### Day 1680 Pandas for Java

Today, I attempted to create a Spark application to perform some data cleaning activities on CSV files. However, I encountered an issue where my application, which uses Java 17, was incompatible with Spark due to errors. After trying different solutions to resolve this problem, I ultimately decided to switch to using Python and Pandas for working with CSV files. I find this approach to be more suitable and efficient. Please don't use a hammer for everything, use the right tool for the work.

### Day 1679 Application Problems and GitHub Issues

Today, I have been testing my [database](https://github.com/pablohdzvizcarra/test-database-txt) application and encountered some errors. It's interesting how even small and obvious errors can go unnoticed until we thoroughly test our code. This experience reminds me of the Agile spirit, where we deliver the Minimum Viable Product (MVP) and continuously improve through iterations. Building a JSON database is not as fast as I initially believed, but it's a valuable learning experience.

### Day 1677-78 Java Path Problems

I am currently facing an issue with Java regarding file path management within the JVM filesystem. Specifically, I am encountering an error when attempting to read files from the root folder in a Java JAR application. While my code works fine in Visual Studio Code and when generating the JAR archive on my local machine, it fails when I move the JAR to a different folder. Tomorrow, I will continue investigating and resolving this error.

### Day 1675-76 Problems Reading All Documents

I am facing with a problem when try to read all the documents from X collection. The problem is I am trying to read file by file, deserialize the each file into a ```Map```, add the map to a ```List``` to finally serialize the ```List<Map>``` into a Json, I don't know why I cannot do this due to some Java errors, maybe I need a rest to recover my batteries, well on the weekend I will have some free time to solve this problem.

### Day 1673-74 Continue with CRUD Database Operations

These days I have been working in my database project, I could implement the Read and Delete operations. I am happy with my current job completed, my project was created following a TDD methodology for this reason I can change/add features in my code fast.

### Day 1672 Serialization and Deserialization

Today I created the basic functionalities for serialization and deserialization in my database implementation, I had some problems when deserialize the content of a file JSON file into a Java String, I am looking for a way to deserialize the Java String into a Java record, the problem is create the code generic to be reused to convert a JSON into X Java record/object.

### Day 1671 Document-based database

Today, I continued working on my own database project. I encountered difficulties when attempting to save records/json into a single file. Initially, I planned to store all the records in a single file, with each table represented as a JSON file. However, this approach proved to be complex and caused issues when inserting multiple records. To address this, I have been researching how MongoDB manages these challenges and exploring the document-based approach.

### Day 1669-70 Creating My Own Java Database

Today, I embarked on a Java project to enhance my programming skills. The objective of this project is to create a basic database that supports CRUD functionalities. I have decided to store the data in JSON files, which will be generated in the project's source directory within a dedicated folder. Throughout this project, I am following the Test-Driven Development (TDD) methodology, allowing me to enjoy the process of coding for a personal project after a long time.

### Day 1667-68 Java Testing

I encountered a challenge today while attempting to create unit tests for a Java class. My goal was to add a new feature to the application, and I wanted to establish unit tests to ensure its quality and maintainability. However, I faced difficulties due to the inherent complexities of testing legacy code, particularly those arising from code dependencies.

While I firmly believe that unit testing is the most effective approach to understanding and validating code behavior, I was unable to fully implement tests within the required timeframe due to the feature's urgency.

### Day 1666 CRLF and LF

Today, I learned why my VSC editor shows LF as the end-of-line sequence value. It was fascinating to discover that Windows uses CRLF (\r\n) and Linux uses LF (\n) for this purpose. The different approaches have historical roots, dating back to the early days of computing. While the reasons may seem outdated today, understanding this legacy adds depth to our appreciation of computer science.

### Day 1665 Continue Reading About Linux

These days I have been reading the Linux command line book. I am reading the book and making excersises in my computer at the same time, it is amazing how the terminal is very powerfull and useful when you lose the fear. Today I had a unconfort situation in my work due to my English skill, I know English is very important in the Software Engineering industry, please if you are reading this, learn English and learn good, talk with people in discord, watch TV in English but the most important thing is practice this skill everyday.

### Day 1661 Synchronous Architectures and Python

Today I was working in a issue related with a [race condition](https://simple.wikipedia.org/wiki/Race_condition) in two Microservices that need to interact between them in the correct order, I saw this problem other times and I performed some exercises in the past to avoid issues using Events to communicate rather than synchronous code and waiting always that the process X finish it is execution before process W starts. Microservice are amazing I love how a simple Microservice design can be converted into a complicated scenario.

### Day 1560 Grep and Linux Dictionary

Today I started to learn about the [grep](https://man.cx/grep(1)) in Linux. I practice performing some grep commands using different Metacharacters like anchors and brackets. Also I discovered that Linux distributions have a dictionary, and yes this is amazing look in the /usr/share/dict/words path. On my work I read the pandas documentation about the [to_dict](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_dict.html) because I need to work with this functionality.

### Day 1559 Python and Flexibility

Today I was working in a task that needs to be performed fast, I choice Python to create and execute the task duw to the Python simplicity and their useful libraries to work with files, I have a lot of desire to learn how to apply TDD for this simple task working with Python, my testing skills in Python are little.

### Day 1556-57-58 Java Http Server

On the weekend I have been learning about the jwebserver, a Java tool to crate a HTTP server for testing purposes. This tool is amazing sometimes we only need a HTTP server to put some information that work as an external API, and another service use this information to perform their work. Also I learned how to create a Java HTTP server for testing purposes mounting a directory hierarchy and some files in the server in memory without save the information in disk, this exercise was amazing.

### Day 1555 Java and Linux

Today I learned more about Maven, I studying which plugins are required to create Java applications packaged into a jar file, how I can create a jar artifact with all the required dependencies to run. Also I continued studying Linux, now is the time to study some tools to find files and directories.

### Day 1554 OpenShift S2I

Today I learned how to create applications in OpenShift with the S2I Strategy builder, was interesting how OpenShift with only a git repository with a app.py file can create and deploy an application fast. Working in creating the previous application I noticed that I don't know how to create a Java application from scratch without use a tool like maven or gradle, my plan is learn how to create a maven project without using the mvn command because in the host that I use I don't have maven installed, tomorrow I will review how to achieve this.

### Day 1553 Data Analytics

Today, I engaged in several data analytics tasks. I am of the opinion that, in the future, AI tools like ChatGPT, which facilitate effortless data analytics, will diminish the significance of this aspect of software engineering. Consequently, I am hesitant to further develop this skill, although it was necessary for my current tasks. Moving forward, I am contemplating aligning my job responsibilities more closely with my long-term goals and steering clear of studying subjects that do not contribute to these objectives.

### Day 1549-52 Linux and OpenShift

These days I continue reading the Linux book, I learned some important file system and network linux commands, also I advanced in my Red Hat certification.

### Day 1548 Linux and Go

Today I continue studying about Linux, I started to study the environment in the shell, now I know what is the use of some Environment variables like HOME, PATH and obviously the JAVA_HOME, some programs use this variables well, don't use the variables use the files reference for this variables remember in Linux everything is a file. Also I practice a little of Go and a sandbox environment, doing a little software exercise.

### Day 1547 Continue with Linux

Today I studied the most useful command linux to manipulate the processes running in the system like top, ps, kill, etc.

### Day 1545-46 Red Hat Course and Linux

Today I have been working in my Red Hat course, I learned more about the ConfigMaps and Secrets resources in OpenShift, creating a basic python http server application that returns the value from a Environment variable, the objective was assign this value with some configuration like take the value from a environment variable or a file.

### Day 1540-44 New Year Coding

As the new year bursts onto the scene, I'm thrilled to set my software engineering goals for 2024! I've meticulously crafted a plan encompassing study initiatives, ambitious project targets, and even the exciting prospect of learning a new programming language. I eagerly anticipate the professional and personal growth this year will bring, brimming with fresh opportunities and challenges.

### Day 1534-40 Holydays with Coding

These holydays I continue to reading my current book, and also I am learning how to use neovim as my IDE, neovim is amazing but very complicated, I am learning a lot of new concepts.  

### Day 1533 Building Containers

Today studying thr Red Hat certification I did a little exercise to build a container image following the best practices recommended by RedHat. I don't know why but Containers and Microservices are two topics loved by me.

### Day 1532 Python ETL

Today I was creating a Python ETL process for run, my idea was extract some data for X source, next apply some cleaning and transformation operations to this data to finally save the data with pandas into a CSV file.

### Day 1531 NeoVim Distractions

Today I send my day learning how to configure NeoVim to work with Java and Python, I am learning new concepts like LSP servers, key mappers and how a editor like Visual Studio Code works under the hood, but I am spending my time in a non important task at this moment, my current goal at this moment is to complete my RedHat certification and finish to read the Linux book. NeoVim is amazing, but is a high-consume thing.

### Day 1528-29-30 Studying Linux

During the weekend I continue working in my certification and learning more about Linux. I learned what is the Expansion in the Linux shell, basically is when we introduce something to the shell and the shell produces something else before execute the command one example can be 'echo *', the shell expand the symbol '*' to a list with all the files and folders in the current directory. Learning about Linux is changing my mind in some topics about Software Engineer, it's interesting how Linux works and how an operating system is build it.

### Day 1527 Environment Issues

Today working with some Python code, I had some problems when executing unit testing in a container environment, in my local visual studio code the unit test work without problems, but in the containerized environment I had an error when executing the unit test. The error was strange, but today I learned how to create a Dockerfile to execute unit test with Python and how to configure a Python project in VSC with venv Python environment.

### Day 1525-26 Linux, Linux and more Linux

These days I continue working in my red hat certification, I am learning useful linux commands like look for files using regex patterns, learn how works with OpenShift pods testing connections between pods to troubleshoot common errors.

### Day 1524 Python and Dependency Injection

Today I ask me what is the reason that dependency injection in python is not a common use technique. I am working in writing python code, the problem is that to mock some database dependency, the best option is to mock the database dependency using the dependency injection technique. With Python the most common option used is mock/patch directly the function.

### Day 1523 Linux and OpenShift

Today I continue learning more about Linux and OpenShift. Working in my Red Hat certification, I learned how to deploy an application using the OpenShift web console, creating a project and deploy an application from an image stored in a container registry.

### Day 1520-21-22 Linux

These days I was studying about Linux, I am working in a Red Hat certification to gain more knowledge about Linux I started to read The Linux Command Line book. In my first days I learned some interesting things like the shell is a program to accept keyboard inputs from the user and send these inputs to the operating system, the most common shell programs are **bash** and **zsh**, also I learned that to interact with a shell we require a terminal emulator like iTerm, I am reading the book at the same time doing some code exercises with Java, creating some abstractions to emulate a operating system in code. I am happy writing code.

### Day 1519 Http Go Server

Today I was writing a HTTP server with golang, I want to know how build a HTTP server with Go only for curiosity because I hear a lot of times that golang is a great language, and well create a basic HTTP server is a easy task.
Golang > Python.  

### Day 1517-18 OpenShift

Today doing my Red Hat certification I studied OpenShift platform, I am happy because I can understand an ambiguous topic in software engineer for me what is a Cluster and a Node? Cluster is a group of servers that work together, and a node is a server inside the cluster. The OpenShift platform uses a node as the master node to control some operations in the OpenShift cluster, but if this node fails, the OpenShift platform can use another node as the master.
Overall, understanding the concept of clusters and nodes is fundamental to understanding how OpenShift platform works. I'm excited to continue learning and exploring its capabilities!

### Day 1515-16 Python Pandas

These days I dedicated some time to learn more about Python pandas library. I will want to have some expertise with Python and basic data analytics task like read data, filter data, transform data and so on. Also I love to write useful Python scripts to automate my daily activities, really help me to save a lot of time in manual work.

### Day 1514 Continue with Executor

Today I have been writing a tutorial to understand what is a Java executor and how you can use a Executor in you Java code. Tomorrow I will investigating about how the Executor works the Go language, I want to understand the abstract concept about this.

### Day 1512-13 Java Executor

Today I have been learning about what is and how works an Executor in Java. I planning to create a Java tutorial trying to understand this concept, I want to learn the abstract concept about an Executor and understand how to works with them with Java and maybe Golang.

### Day 1511 Java Optional

Today I created an elegant solution to a Java problem, I will need to call a method to get something, if this X item exists do action A and if doesn't exists do action B, I have the idea to return a Java optional from the calling method an use the ifPresentOrElse method from the Java optional rather than a if statement.
The result code was elegant and beautiful.

### Day 1510 Java JFR

Today I was learning more about the JFR tool due to some performance issues in my work related with high CPU usage for a Java application.

### Day 1509 Visual Studio Code Problems

Today I was reading the Settings Sync Visual Studio Code documentation, I am having some problems with sync my editor configuration. Maybe I will need to continue solving this issue tomorrow.

### Day 1508 Continuing with Reading

Today, I delved further into the "Software Developer Career" book, focusing on its second chapter, which delves into the Mindset for Career and Life. The book provides valuable insights into enhancing one's self-esteem, vital for both personal growth and becoming a better software developer. Reading through it, I experienced several 'aha' moments, gaining new psychological insights that shed light on various topics. The book's exercises aided in understanding my career perspective and contemplating my thoughts.

### Day 1507 Completed Course

Today I completed the Introduction to Containers with Podman course for the Cloud-Native Certified Developer.
In this course I refresh and learn new things about Containers. I learned a interesting thins like manage container lifecycle, manage network and volumes with Podman, also how to create Database Containers. I love how Podman wants to facilitate the container deployment in a local Kubernetes cluster to test applications in local environment.

### Day 1506 OpenShift Container Platform

Today I was studying about the OpenShift platform. I have been doing the Red Hat certification for one month, really  Red Hat things sometimes are hard. But I want to be a Red Hat Certified Cloud Native Developer. OpenShift platform is a great piece of software, I don't know why but I love work with Containers and Kubernetes.

### Day 1505 Implementing SELinux System

Today I worked in a little implementation of the SELinux system with Java code. I wrote a label, object and a folder classes to represent the label and the objects in the SELinux mechanism. Also I created a SELinux component to validate that some user with X label has access to the folder with the X label. Project-Based learning is really a great way to learn software engineering concepts.

### Day 1504 SELinux

Today I did a little study about the SELinux system. The Security-Enhanced Linux is a security architecture system to control the resources access into a linux system, resources like files, processes and folders. SELinux works as a labeled system to give access to the subjects/users.

### Day 1502-03 Scala and Spark

These two days I am learning how to create a uber jar file given a Scala project. Really I waste a lot of time looking tutorials in the internet, finally I found the answer in the sbt-assembly-plugin official documentation. Please first read the documentation before look for an answer in the internet or ChatGPT.
Tomorrow I will need to continue developing my Scala and Spark application.

**Day 1 - 50 HTML - CSS - Javascript**  [here](./day0-500/day0-50.md)</br>
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
